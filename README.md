MySQLPivot
==========

(check this readme in raw mode because I couldn't find a way to show the examples as matrix, but in raw mode yes!)

MySQL Pivot Query (convert a table or query in a 2-dim matrix)

I've made a couple of routines for something that is hardly missing in MySQL: pivot tables.

Sometimes you want to show a table with certain results in a easier-to-read matrix.

Example:

person1, hour1, value1
person2, hour2, value2
person1, hour2, value3
person1, hour3, value4
person2, hour3, value5

You want to see it as:

         hour1   hour2   hour3
person1  value1  value3  value4
person2          value2  value5

Or so.

One of the routines do that. The other adds totals to each row, column, and a global total, like:

         total    hour1    hour2    hour3
0_total  global   t_hour1  t_hour2  t_hour3
person1  t_per1   value1   value3   value4
person2  t_per2   value2   value5

In every routine:

query2 it's the query where the data (and all fields) comes from.
ct is the field with the column titles
rt is the field with the row titles
dd is the field with the data for the matrix.

columns are sorted alphabetically, rows too.

A comment about legal stuff: you can use these routines any way you want, to get money or not, just don't hurt anybody with them. I let you to take all risks and full responsability using these routines, and please mention me as the author of this code whenever possible and this source point in GitHub so anybody can come here if they want.

One last comment: these routines are not perfect. They just do the job.

Enjoy!


