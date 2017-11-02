# DAND_Module1_Practice
python读取各种各样的数据

# CVS

### parsecsv.py

使用 CSV 模块

你的任务是处理提供的文件，并使用 csv 模块从中提取文件。数据来自国家可再生能源实验室 (NREL) 网站。每个文件都包含来自某个气象站的信息，尤其是关于一天当中每小时的太阳能和风能数量。

注意，数据文件的第一行既不是数据项，也不是标题。它是用来描述数据来源的行。你应该从该行中提取气象站名称。

数据应该返回为包含列表的列表（而不是字典）。你可以使用模块“reader”方法获取此类格式的数据。另一个有用的方法是next()，可以用来获取迭代器中的下一行。你只需更改parse_file 函数。

数据来自 [NREL 网站](http://www.nrel.gov/)。此练习中的数据文件是其中一个站点的完整文件的小型子集。你可以从下方的“课程材料”中下载该数据文件，或者查看[全国太阳辐射数据库](http://rredc.nrel.gov/solar/old_data/nsrdb/1991-2005/tmy3/by_USAFN.html)上其他站点的完整数据文件。
 
# Excel

### excel_csv.py

Excel 至 CSV

计算以下每个地区的最大加载时间和值：COAST、EAST、FAR_WEST、NORTH、NORTH_C、SOUTHERN、SOUTH_C、WEST，并将结果写到 csv 文件中，使用竖线字符“|”作为分隔符。

可以在“example.csv”文件中查看示例输出。
查看 [csv 模块文档](http://docs.python.org/2/library/csv.html)，了解如何针对 csv.writer 使用不同的分隔符。

你可以从辅助材料中下载数据文件 2013 ERCOT Hourly Load Data。

# Json

### nytimss.py

此示例展示了你应该了解的一些重要概念：
- 如何使用编解码模块编写 Unicode 文件
- 如何使用网络 API 进行身份验证
- 在访问网络 API 时如何使用偏移

要在本地运行这段代码，你需要在 NYTimes 开发者网站进行注册，并获取你自己的 API 密钥。当然，不进行注册也可以在我们的 UI 中完成此练习，因为我们已经提供了示例结果（请参阅上述标签中的“popular-viewed-1.json”）。

你的任务是修改 article_overview() 函数以处理表示前一天最热门文章（按阅读数量排名）的已保存文件，并返回一个变量元祖，其中包含以下数据：
- 标签：字典列表，其中键是“版块”值，值是每个所检索的文章的“标题”值。
- URL：所有“media”条目的 URL 列表，“格式”为：标准缩略图

你只需对article_overview() 函数做出更改。请参阅test() 函数，了解输出列表的元素示例。其他函数只是便于你自己访问相关 API。

如果你想了解更多信息，或想自行查询网站，请阅读[针对最受欢迎API的《纽约时报》开发者文档](http://developer.nytimes.com/docs/most_popular_api)和[为《纽约时报》申请你自己的 API 密钥](http://developer.nytimes.com/page)。

# Xml

### authors.py

提取数据

你的任务是从 xml 中提取关于文章作者的数据， 并将其添加到列表中，一个作者对应一个条目。 
请参阅提供的数据结构，了解我们期望的格式。
名字、姓氏和电子邮箱标签应该直接对应字典关键字

处理属性
[ElementTree 文档](http://docs.python.org/2/library/xml.etree.elementtree.html#module-xml.etree.ElementTree)

你的任务是从 xml 中提取关于文章作者的数据，并将其添加到列表中，一个作者对应一个条目。
请参阅提供的数据结构，了解我们期望的格式。
名字、姓氏和电子邮箱标签应该直接对应字典关键字，但是你需要从"insr"标签中提取属性，并将其添加到字典关键字“insr”列表中

### patent.py

专利数据库

查看下一道测试题，以了解与该 XML 文件有关的特定问题。

这道练习和下面的练习使用的是美国专利数据库。patent.data 文件是一个更加庞大的数据文件（可以从美国专利网站上下载）的摘要部分。这些文件非常大（每个都超过 100 MB）。原始文件大概 600 MB，你可能无法在文本编辑器中打开这些文件。

数据本身是 XML 格式，但是格式存在问题。请运行此脚本并观察错误。然后找到导致错误的行。你可以直接在网络 UI 中查看数据文件，或者通过程序方式找到错误的行。对于这道测验，哪种方法都可以，但是建议你采用程序方式。

注意：你不需要纠正该错误，暂时只需知道错误所在的行。

### split_data.py
处理专利

问题是庞大的文件实际上不是有效的 XML，因为它有几个根元素和 XML 声明。
实际上是多个相连的 XML 文档构成的。一种解决方法是将文件拆分为多个文档，
并将这些文档处理为有效的 XML 文档。

# HTML

### html_soup.py 

使用 Beautiful Soup
[Beautiful Soup 文档](http://www.crummy.com/software/BeautifulSoup/bs4/doc/)

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

对于这道练习，你的任务是修改“extract_carrier()”，以便获取所有航空公司列表。请在返回的数据中删除所有的组合值，例如“All U.S. Carriers”。你应该返回一个航空公司代码列表。

你只需更改“extract_carrier()”函数。上述标签中的“options.html”文件是网站实际版本的缩减版，但是可以帮助你大概了解完整文件的样貌。

请注意，函数“make_request()”仅供参考。你实际上无法在优达学城的网络 UI 中使用该函数。

### airports.py

练习: 机场列表

请完成“extract_airports()”函数，使其返回机场代码列表，并删除任何组合内容，例如“All”。

请参阅上述标签中的“options.html”文件，了解实际网站的缩减版。test() 声明是基于给定的文件。

### process.py

处理所有数据

假设你将上两个练习中的代码与关于如何构建请求的课程中代码相结合，并将所有数据下载到了本地。文件位于目录“data”下，按照航空公司和机场命名："{}-{}.html".format(carrier, airport)，例如“FL-ATL.html”。

包含航班信息的表格具有一个表格类“dataTDRight”。你的任务是使用“process_file()”从该表格中提取航班数据，并作为字典列表，每个字典包含文件中的相关信息和表格行。以下是你应该返回的数据结构示例：

Note - year, month, and the flight data should be integers.
You should skip the rows that contain the TOTAL data for a year.
注意：年月和航班数据应该是整型。你应该跳过包含一年 TOTAL 数据的行。

你可以使用几个辅助函数来处理数据文件。为了方便打分，请勿更改这些辅助函数。你只需更改“process_file()”函数。

上述标签中的“data/FL-ATL.html”文件只是完整数据的一部分，涵盖的是截止 2003 年的数据。test() 代码将使用完整的表格，但是给定文件应该提供一个你将获得的数据示例。

# 数据质量

### validity.py

 修正有效性
你可以从[课程资源](https://www.udacity.com/wiki/ud032#datasets-used-in-this-course)下载数据文件。

你的任务是检查 DBPedia 自动数据文件的“productionStartYear”并获取有效的值。应该完成以下任务：
- 检查字段“productionStartYear”是否包含年份
- 检查该年份是否在 1886 至 2014 范围内
- 将字段值转换为年份（而不是整个日期时间）
- 字段的其他部分和值应该保持不变
- 如果字段的值是如上所述范围内的有效年份，则将该行写入 output_good 文件中
- 如果字段的值不是如上所述的有效年份，则将该行写入 output_bad 文件中
- 你应该采用提供的数据读取和写入方式（DictReader 和 DictWriter），它们将会对标题进行处理。

你可以编写辅助函数来检查数据并编写文件，但是我们将仅调用包含三个参数（inputfile、output_good、output_bad）的“process_file”文件。

### audit.py

审查数据质量

你可以从[课程材料](https://www.udacity.com/wiki/ud032#datasets-used-in-this-course)中下载完整的数据文件。为了进行评分，你的代码将和“在线代码编辑器”选项卡上的 cities.csv 子集进行匹配，因此，如果你是在本地对完整的数据集运行代码，测试断言可能会不匹配。

在此习题集中，你将处理城市 infobox 数据，对数据进行审核，然后想出清理方法并清理数据。在第一道练习中，请审核数据集中某些特定字段中的数据类型。
值类型可以是：
- NoneType，如果值是字符串“NULL”或空字符串“”
- 列表，如果值以“{”开头
- 整型，如果值可以转型为整型
- 浮点型，如果值可以转型为浮点型，但是无法转型为整型。
例如，“3.23e+07”应该被当做浮点型，因为可以转型为浮点型，但是int('3.23e+07') 将抛出 ValueError
- “str”，表示其他所有值

audit_file 函数应该返回一个字典，其中包含字段名称和可以在该字段中找到的类型集。例如
{"field1": set([type(float()), type(int()), type(str())]),
 "field2": set([type(str())]),
  ....
}
type() 函数返回的是类型对象，描述了提供给该函数的参数。你还可以使用对象示例创建类型对象，例如 type(1.1) 表示浮点型：具体示例请参阅下面的测试函数。

注意，cities.csv 文件的前三行（标题行之后）不是实际的数据点。在处理数据类型时，不应该包含这些行的内容。确保在代码中包含相关功能，以便跳过或检测出这些行。

### area.py

修复区域
你可以从[课程材料](https://www.udacity.com/wiki/ud032#datasets-used-in-this-course)中下载完整的数据文件。为了进行评分，你的代码将和“在线代码编辑器”选项卡上的 cities.csv 子集进行匹配，因此，如果你是在本地对完整的数据集运行代码，测试断言可能会不匹配。

在此习题集中，你将处理城市 infobox 数据，对数据进行审核，然后想出清理方法并清理数据。

因为在上一道测验中，你已经决定针对“areaLand”字段保留哪个值，你现在知道该如何操作了。

完成函数 fix_area()。它将获得字符串输入，并需要返回表示面积值的浮点值或 None。你需要更改fix_area 函数。你可以使用其他函数，但是对 process_file 的更改不会计入评估范围。代码的其余部分只是用来展示可以如何使用该函数的示例。

### name.py

修复姓名

在此习题集中，你将处理城市 infobox 数据，对数据进行审核，然后想出清理方法并清理数据。

在上一道测验中，你意识到“name”值可以是数组（或用 Python 术语来说的话，是列表）。如果名称的所有值是 Python 列表（而不是用特殊字符分隔的字符串，例如现在的状况），则稍后更容易处理和查询数据。

请完成函数fix_name()。它将获得字符串输入，并返回所有名称列表。如果只有一个名称，列表将只有一项。如果名称是“NULL”，该列表应该为空。代码的其余部分只是可以用来展示如何使用该函数的示例。

