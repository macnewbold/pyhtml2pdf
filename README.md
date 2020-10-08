# pyhtml2pdf
Simple python wrapper to convert HTML to PDF with headless Chrome via selenium.

**Use with website url**

```
from pyhtml2pdf import converter

converter.convert('https://pypi.org', 'sample.pdf')
```

**Use with html file from local machine**

```
import os
from pyhtml2pdf import converter

path = os.path.abspath('index.html')
converter.convert(f'file:///{path}', 'sample.pdf')
```

**Some JS objects may have animations or take a some time to render. You can set a time out in order to help render those objects. You can set timeout in seconds**

```
converter.convert(source, target, timeout=2)
```

Inspired the work from https://github.com/maxvst/python-selenium-chrome-html-to-pdf-converter.git