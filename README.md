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

### authors.py

提取数据

Your task here is to extract data from xml on authors of an article and add it to a list, one item for an author. See the provided data structure for the expected format. The tags for first name, surname and email should map directly to the dictionary keys

你的任务是从 xml 中提取关于文章作者的数据， 并将其添加到列表中，一个作者对应一个条目。 
请参阅提供的数据结构，了解我们期望的格式。
名字、姓氏和电子邮箱标签应该直接对应字典关键字

处理属性
[ElementTree 文档](http://docs.python.org/2/library/xml.etree.elementtree.html#module-xml.etree.ElementTree)

Your task here is to extract data from xml on authors of an article and add it to a list, one item for an author. See the provided data structure for the expected format. The tags for first name, surname and email should map directly to the dictionary keys, but you have to extract the attributes from the "insr" tag and add them to the list for the dictionary key "insr"

你的任务是从 xml 中提取关于文章作者的数据，并将其添加到列表中，一个作者对应一个条目。
请参阅提供的数据结构，了解我们期望的格式。
名字、姓氏和电子邮箱标签应该直接对应字典关键字，但是你需要从"insr"标签中提取属性，并将其添加到字典关键字“insr”列表中

### patent.py

专利数据库

查看下一道测试题，以了解与该 XML 文件有关的特定问题。

This and the following exercise are using US Patent database. The patent.data
file is a small excerpt of much larger datafiles that are available for
download from US Patent website. These files are pretty large ( >100 MB each).
The original file is ~600MB large, you might not be able to open it in a text
editor.

这道练习和下面的练习使用的是美国专利数据库。patent.data 文件是一个更加庞大的数据文件（可以从美国专利网站上下载）的摘要部分。这些文件非常大（每个都超过 100 MB）。原始文件大概 600 MB，你可能无法在文本编辑器中打开这些文件。

The data itself is in XML, however there is a problem with how it's formatted.
Please run this script and observe the error. Then find the line that is
causing the error. You can do that by just looking at the datafile in the web
UI, or programmatically. For quiz purposes it does not matter, but as an
exercise we suggest that you try to do it programmatically.

数据本身是 XML 格式，但是格式存在问题。请运行此脚本并观察错误。然后找到导致错误的行。你可以直接在网络 UI 中查看数据文件，或者通过程序方式找到错误的行。对于这道测验，哪种方法都可以，但是建议你采用程序方式。

NOTE: You do not need to correct the error - for now, just find where the error
is occurring.

注意：你不需要纠正该错误，暂时只需知道错误所在的行。

### split_data.py
处理专利

So, the problem is that the gigantic file is actually not a valid XML, 
because it has several root elements, and XML declarations.
It is, a matter of fact, a collection of a lot of concatenated XML documents.
So, one solution would be to split the file into separate documents,
so that you can process the resulting files as valid XML documents.

问题是庞大的文件实际上不是有效的 XML，因为它有几个根元素和 XML 声明。
实际上是多个相连的 XML 文档构成的。一种解决方法是将文件拆分为多个文档，
并将这些文档处理为有效的 XML 文档。

# HTML

### html_soup.py 

使用 Beautiful Soup
[Beautiful Soup 文档](http://www.crummy.com/software/BeautifulSoup/bs4/doc/)

Please note that the function 'make_request' is provided for your reference only.
You will not be able to to actually use it from within the Udacity web UI.
Your task is to process the HTML using BeautifulSoup, extract the hidden form field values for "__EVENTVALIDATION" and "__VIEWSTATE" and set the appropriate values in the data dictionary.
All your changes should be in the 'extract_data' function

请注意，函数“make_request”仅供参考。
你实际上无法在优达学城的网络 UI 中使用该函数。
你的任务是使用 BeautifulSoup 处理 HTML，提取出"__EVENTVALIDATION”和“__VIEWSTATE”的隐藏表格字段值，并在数据字典中设置相应的值。
你只需更改“extract_data”函数

### carriers.py

运营商列表

说明

请注意函数 'make_request' 仅供为参考。实际情况中，你是无法从优达学城的网页 UI 中使用它的。你所有的修改都应该在函数 'extract_carrier' 中。并且注意该 html 文件是基于原网页删减过的版本。

这个练习中，你的任务是获取一个包含所有航空公司的列表。在你所返回的数据中要去掉所有类似 “All U.S. Carriers” 的组合。最终你应该返回一个含有运营商编码的列表。

如果你只想在本地查看完整的 HTML 文件，你可以从原始 TranStats 网站下载。

Your task in this exercise is to modify 'extract_carrier()` to get a list of
all airlines. Exclude all of the combination values like "All U.S. Carriers"
from the data that you return. You should return a list of codes for the
carriers.

对于这道练习，你的任务是修改“extract_carrier()”，以便获取所有航空公司列表。请在返回的数据中删除所有的组合值，例如“All U.S. Carriers”。你应该返回一个航空公司代码列表。

All your changes should be in the 'extract_carrier()' function. The
'options.html' file in the tab above is a stripped down version of what is
actually on the website, but should provide an example of what you should get
from the full file.

你只需更改“extract_carrier()”函数。上述标签中的“options.html”文件是网站实际版本的缩减版，但是可以帮助你大概了解完整文件的样貌。

Please note that the function 'make_request()' is provided for your reference
only. You will not be able to to actually use it from within the Udacity web UI.

请注意，函数“make_request()”仅供参考。你实际上无法在优达学城的网络 UI 中使用该函数。

### airports.py

练习: 机场列表

Complete the 'extract_airports()' function so that it returns a list of airport codes, excluding any combinations like "All".

请完成“extract_airports()”函数，使其返回机场代码列表，并删除任何组合内容，例如“All”。

Refer to the 'options.html' file in the tab above for a stripped down version
of what is actually on the website. The test() assertions are based on the
given file.

请参阅上述标签中的“options.html”文件，了解实际网站的缩减版。test() 声明是基于给定的文件。

### process.py

处理所有数据

Let's assume that you combined the code from the previous 2 exercises with code
from the lesson on how to build requests, and downloaded all the data locally.
The files are in a directory "data", named after the carrier and airport:
"{}-{}.html".format(carrier, airport), for example "FL-ATL.html".

假设你将上两个练习中的代码与关于如何构建请求的课程中代码相结合，并将所有数据下载到了本地。文件位于目录“data”下，按照航空公司和机场命名："{}-{}.html".format(carrier, airport)，例如“FL-ATL.html”。

The table with flight info has a table class="dataTDRight". Your task is to
use 'process_file()' to extract the flight data from that table as a list of
dictionaries, each dictionary containing relevant data from the file and table
row. This is an example of the data structure you should return:

包含航班信息的表格具有一个表格类“dataTDRight”。你的任务是使用“process_file()”从该表格中提取航班数据，并作为字典列表，每个字典包含文件中的相关信息和表格行。以下是你应该返回的数据结构示例：

Note - year, month, and the flight data should be integers.
You should skip the rows that contain the TOTAL data for a year.
注意：年月和航班数据应该是整型。你应该跳过包含一年 TOTAL 数据的行。

There are couple of helper functions to deal with the data files.
Please do not change them for grading purposes.
All your changes should be in the 'process_file()' function.

你可以使用几个辅助函数来处理数据文件。为了方便打分，请勿更改这些辅助函数。你只需更改“process_file()”函数。

The 'data/FL-ATL.html' file in the tab above is only a part of the full data,
covering data through 2003. The test() code will be run on the full table, but
the given file should provide an example of what you will get.

上述标签中的“data/FL-ATL.html”文件只是完整数据的一部分，涵盖的是截止 2003 年的数据。test() 代码将使用完整的表格，但是给定文件应该提供一个你将获得的数据示例。

# 数据质量

### validity.py

 修正有效性
你可以从[课程资源](https://www.udacity.com/wiki/ud032#datasets-used-in-this-course)下载数据文件。

Your task is to check the "productionStartYear" of the DBPedia autos datafile for valid values.
The following things should be done:
- check if the field "productionStartYear" contains a year
- check if the year is in range 1886-2014
- convert the value of the field to be just a year (not full datetime)
- the rest of the fields and values should stay the same
- if the value of the field is a valid year in the range as described above,
  write that line to the output_good file
- if the value of the field is not a valid year as described above, 
  write that line to the output_bad file
- discard rows (neither write to good nor bad) if the URI is not from dbpedia.org
- you should use the provided way of reading and writing data (DictReader and DictWriter)
  They will take care of dealing with the header.

你的任务是检查 DBPedia 自动数据文件的“productionStartYear”并获取有效的值。应该完成以下任务：
- 检查字段“productionStartYear”是否包含年份
- 检查该年份是否在 1886 至 2014 范围内
- 将字段值转换为年份（而不是整个日期时间）
- 字段的其他部分和值应该保持不变
- 如果字段的值是如上所述范围内的有效年份，则将该行写入 output_good 文件中
- 如果字段的值不是如上所述的有效年份，则将该行写入 output_bad 文件中
- 你应该采用提供的数据读取和写入方式（DictReader 和 DictWriter），它们将会对标题进行处理。

You can write helper functions for checking the data and writing the files, but we will call only the 
'process_file' with 3 arguments (inputfile, output_good, output_bad).

你可以编写辅助函数来检查数据并编写文件，但是我们将仅调用包含三个参数（inputfile、output_good、output_bad）的“process_file”文件。