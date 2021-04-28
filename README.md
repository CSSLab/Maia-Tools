# Maia-Helper

## Tools
+ Connecting to the server
  + The server is running Ubuntu Linux 18.04 LTS, which is very popular so searching for help hsould be possible
  + Most of the time you'll connect via SSH `ssh USERNAME@dev.maiachess.com`
  + Then it's a standard bash/Linux enviroment
  + VS code has a very nice system for opening remote directories over ssh
    + https://code.visualstudio.com/docs/remote/remote-overview
+ Python 3
  + pandas
  + numpy
  + sqlalchemy
    + with `psycopg2-binary`
  + matplotlib
    + seaborn
  + Jupyter notbooks
  + `pip install numpy psycopg2-binary pandas  SQLAlchemy matplotlib seaborn jupyter`
  + Using a local Anaconda install with a virtual env is a bit of work but makes things easier in the long run
    + https://conda.io/projects/conda/en/latest/user-guide/install/linux.html
+ Jupyter
    + These lines in the config will allow remote connections, if you assign an open port
    + `jupyter notebook --generate-config` will make the config file
    + `jupyter notebook list` will tell you the connection token
```
c.NotebookApp.open_browser = False
c.NotebookApp.port = OPEN_PORT
c.NotebookApp.ip = '*'
```
+ Postgres
  + The postgres SQL database is running you can connect to it directly with `psql`
  + Opening a table with pandas is `df = pandas.read_sql_table('summary_per_game_predictions','postgresql:///lichess')`
+ Git
  + Please commit you code regularly and push to a repo on Github
+ Meeting notes
  + Before meetins having some bullet points in a shared google doc will be helpful.
  + Using the same doc every week means we can easily keep track of things
  + Please also take notes during the meeting
