# pdfbookmark
Automatically generate bookmarks for pdf; 自动为pdf生成书签

需要依赖包, 请下载:
```
pip install PyPDF2
```
## 流程
+  请将文件 {pdfname}.pdf 放到pdf文件夹中
+ 请将文件pdf的目录 {pdfname}.txt 放到mark文件夹中
+ 运行main.ipynb
+ 结果会放在marked_pdf文件夹里

>## 注意事项
>* 章的格式: 第1章 预备知识 1
>* 节的格式: 1.2 C++简史 2
>* 字节的格式: 1.2.1 C语言 2

如果您的书签不是以上这样, 那就需要在main.ipynb中修改以下的内容:

(这里需要少许python re知识)
```
chapter_pattern = r'^(第+\d+章+\s+\S+)\s+(\d+)$'
part1_pattern = r'^(\d+\.\d+\s+\S+)\s+(\d+)$'
part2_pattern = r'^(\d+\.\d+\.\d+\s+\S+)\s+(\d+)$'
