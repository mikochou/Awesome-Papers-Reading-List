# Tidy Data
http://vita.had.co.nz/papers/tidy-data.pdf

1. What is the problem that is being solved?
make data preparation easier-data tidying
structuring datasets to facilitate analysis

2. methods
This paper comes up with five most common problems and ways to solve them.
* Column headers are values, not variable names. -> melt it就是把值提取出来，作为一个单独的列，取一个变量名。
* Multiple variables are stored in one column.  -> 多个变量混合，那就把变量分开作为不同的列
* Variables are stored in both rows and columns.  -> 如果列中含有变量名，就要提取出来，不能作为变量的值
* Multiple types of observational units are stored in the same table. -> 对于重复的数据（行为），可以把表拆分
*  A single observational unit is stored in multiple tables. -> 将文件读入表格列表，对于每个表，添加一个记录原始文件名的新列，将所有表组合成一个表。

3. case study
[tidy-data](https://github.com/hadley/tidy-data/tree/master/case-study)
