docker run -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=aA#123456" \
   -p 1433:1433 --name sql1 -h sql1 \
   -d mcr.microsoft.com/mssql/server:2019-latest \
  

docker exec -it sql1 "bash"

/opt/mssql-tools/bin/sqlcmd -S localhost -U SA -P "3637"


/opt/mssql-tools/bin/sqlcmd -S localhost -U SA -P "aA#123456"

CREATE DATABASE TestDB



