Query Impala in R
=================

## Dependencies
- R package `RJDBC` -> allows R to connect to any DBMS that has a JDBC driver
- Impala JDBC Drivers

## Usage

- Fill in the variable `impalaConnectionUrl`, the url used to open a connection on Impala
- Replace the value `impala_jdbc_folder_path` with the name of the impala drivers folder in the function `JDBC()`
- Replace the value of the database parameter `dbname` in the function `dbConnect()` with the target database name
- If your system is a Windows, add this code in the beginning in your script :
  # Load/Download DBI library
  if(!require("DBI")){
    install.packages("DBI", repos = "http://cran.r-project.org")
    library("DBI")
  }
  # Load/Download rJava library
  if(!require("rJava")){
    install.packages("rJava", repos = "http://cran.r-project.org")
    library("rJava")
  }
  # JAVA_HOME = ""
  if(Sys.getenv("JAVA_HOME")!="")
    Sys.setenv(JAVA_HOME="")
  library(rJava)


