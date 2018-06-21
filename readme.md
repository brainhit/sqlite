apt-get install sqlite3

import sqlite3
conn = sqlite3.connect('test.db') # create a test.db file in the local folder
conn.execute("create table test (id int, url string)")
conn.execute("insert into table values (1, 'www.google.com')")
conn.commit()
cursor = conn.execute("select * from test")
for row in cursor:
	print(row)
conn.close()

sqlite3 test.db
.databases # show databases
.tables # show tables
