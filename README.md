# Thesis-work
# Create a directory and call it anything you want
mkdir -p caravel_tutorial

# navigate into the directory
cd caravel_tutorial

# Make sure that "caravel_example" matches the empty github repo name in step 1
git clone -b mpw-6b https://github.com/efabless/caravel_user_project caravel_example
cd caravel_example
git remote rename origin upstream

# You need to put your empty github repo URL from step 1
git remote add origin <your github repo URL>

# Create a new branch, you can name it anything
git checkout -b <my_branch>
git push -u origin <my_branch>
  
# make sure to change <directory_name> with the directory you created in step 2
# in this case it is caravel_tutorial
export OPENLANE_ROOT=~/<directory_name>/openlane # you need to export this whenever you start a new shell

export PDK_ROOT=~/<directory_name>/pdks # you need to export this whenever you start a new shell

make setup
