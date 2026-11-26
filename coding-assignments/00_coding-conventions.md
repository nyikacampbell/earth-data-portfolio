# Coding Conventions
For notebooks in the coding-assignments folder

* write out results using the shared paths from `setup-filepaths.ipynb` (`portfolio_dir`, `assignments_dir`, `img_dir`, `posts_dir`) instead of hardcoded or home-relative paths
  * example to create paths
  ```python
  ### Make path
  ndvi_dir = os.path.join(
    portfolio_dir, "coding-assignments", "03_vegetation", "data", "06_ndvi"
  )
  ### then make folder
  os.makedirs(boundary_dir, exist_ok=True)

  ### make folders paths because they aren't already
  boundary_dir = pathlib.Path(boundary_dir)
  ```
  
boundary_dir, ndvi_dir
* read downloaded or generated data into the assignment's own `data/` folder
  * create the folder by adding a `data/.keep` file — the folder itself is tracked in git, but everything else inside `data/` is git-ignored
* end every notebook with a `%store` of any variables later notebooks will need, followed by a run timestamp:
  ```python
  %store var1 var2
  ### print code run date and time
  print(f"Code Done as of: {pd.Timestamp.now()}")
  ```
  * retrieve with
  ```python
  %store -r
  ```
