# DAND_Module1_Practice
python读取各种各样的数据

# CVS

### parsecsv.py

使用 CSV 模块

Your task is to process the supplied file and use the csv module to extract data from it.
The data comes from NREL (National Renewable Energy Laboratory) website. Each file
contains information from one meteorological station, in particular - about amount of
solar and wind energy for each hour of day.

你的任务是处理提供的文件，并使用 csv 模块从中提取文件。数据来自国家可再生能源实验室 (NREL) 网站。每个文件都包含来自某个气象站的信息，尤其是关于一天当中每小时的太阳能和风能数量。

Note that the first line of the datafile is neither data entry, nor header. It is a line
describing the data source. You should extract the name of the station from it.

注意，数据文件的第一行既不是数据项，也不是标题。它是用来描述数据来源的行。你应该从该行中提取气象站名称。

The data should be returned as a list of lists (not dictionaries).
You can use the csv modules "reader" method to get data in such format.
Another useful method is next() - to get the next line from the iterator.
You should only change the parse_file function.

数据应该返回为包含列表的列表（而不是字典）。你可以使用模块“reader”方法获取此类格式的数据。另一个有用的方法是next()，可以用来获取迭代器中的下一行。你只需更改parse_file 函数。

数据来自 [NREL 网站](http://www.nrel.gov/)。此练习中的数据文件是其中一个站点的完整文件的小型子集。你可以从下方的“课程材料”中下载该数据文件，或者查看[全国太阳辐射数据库](http://rredc.nrel.gov/solar/old_data/nsrdb/1991-2005/tmy3/by_USAFN.html)上其他站点的完整数据文件。
 
# Excel

### excel_csv.py

Excel 至 CSV

Find the time and value of max load for each of the regions
COAST, EAST, FAR_WEST, NORTH, NORTH_C, SOUTHERN, SOUTH_C, WEST
and write the result out in a csv file, using pipe character | as the delimiter.

计算以下每个地区的最大加载时间和值：COAST、EAST、FAR_WEST、NORTH、NORTH_C、SOUTHERN、SOUTH_C、WEST，并将结果写到 csv 文件中，使用竖线字符“|”作为分隔符。

An example output can be seen in the "example.csv" file.

可以在“example.csv”文件中查看示例输出。
查看 [csv 模块文档](http://docs.python.org/2/library/csv.html)，了解如何针对 csv.writer 使用不同的分隔符。

你可以从辅助材料中下载数据文件 2013 ERCOT Hourly Load Data。

# Json

### nytimss.py

This exercise shows some important concepts that you should be aware about:
- using codecs module to write unicode files
- using authentication with web APIs
- using offset when accessing web APIs

此示例展示了你应该了解的一些重要概念：
- 如何使用编解码模块编写 Unicode 文件
- 如何使用网络 API 进行身份验证
- 在访问网络 API 时如何使用偏移

To run this code locally you have to register at the NYTimes developer site 
and get your own API key. You will be able to complete this exercise in our UI
without doing so, as we have provided a sample result. (See the file 
'popular-viewed-1.json' from the tabs above.)

要在本地运行这段代码，你需要在 NYTimes 开发者网站进行注册，并获取你自己的 API 密钥。当然，不进行注册也可以在我们的 UI 中完成此练习，因为我们已经提供了示例结果（请参阅上述标签中的“popular-viewed-1.json”）。

Your task is to modify the article_overview() function to process the saved
file that represents the most popular articles (by view count) from the last
day, and return a tuple of variables containing the following data:
- labels: list of dictionaries, where the keys are the "section" values and
  values are the "title" values for each of the retrieved articles.
- urls: list of URLs for all 'media' entries with "format": "Standard Thumbnail"

你的任务是修改 article_overview() 函数以处理表示前一天最热门文章（按阅读数量排名）的已保存文件，并返回一个变量元祖，其中包含以下数据：
- 标签：字典列表，其中键是“版块”值，值是每个所检索的文章的“标题”值。
- URL：所有“media”条目的 URL 列表，“格式”为：标准缩略图


All your changes should be in the article_overview() function. See the test() 
function for examples of the elements of the output lists.
The rest of functions are provided for your convenience, if you want to access
the API by yourself.

你只需对article_overview() 函数做出更改。请参阅test() 函数，了解输出列表的元素示例。其他函数只是便于你自己访问相关 API。

如果你想了解更多信息，或想自行查询网站，请阅读[针对最受欢迎API的《纽约时报》开发者文档](http://developer.nytimes.com/docs/most_popular_api)和[为《纽约时报》申请你自己的 API 密钥](http://developer.nytimes.com/page)。

# Xml

