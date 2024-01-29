# 笔记

## 测试图片展示

![Alt text](<Clipboard - 2023-12-20 12.49.05.png>)

## Markdown 语法测试

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## 项目结构

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.


## 配置 
### Content tabs
todo 使用 iconfont 显示特殊图标
``` { .yaml .select }
markdown_extensions:
  - pymdownx.superfences
  - pymdownx.tabbed:
      alternate_style: true
```

=== ":simple-windows11: Win"

    ``` python
    import time
    time.sleep(1)  # (1)!
    ```

    1. 程序暂停一秒


=== ":fontawesome-brands-apple: Mac"

    ``` sh title="bubble_sort.py"
    # Code block content
    pip install mkdocs-material=="9.*"
    ```

=== ":simple-linux: Linux"

    ``` sh
    # Code block content
    pip install mkdocs-material=="9.*"
    ```


### 代码块添加标题、行号

``` py title="bubble_sort.py" linenums="1"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

### 突出显示特定行
``` py hl_lines="2 3"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

### 嵌入外部文件
``` json title="test.json"
--8<-- "test.json"
```

