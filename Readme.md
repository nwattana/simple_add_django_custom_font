# เพิ่มFont ให้ Django
ตัวอย่าง การเพิ่ม Fonts เอง ในdjango
- โหลด Font มา
- set Static root ใน setting.py
- เก็บไฟล ไว้ใน Static folder ของ Project
| /app/appfe/static/fonts/BrisoProItalic.otf


### example code
<a url="/appfe/templete/simple.html">FILE</a>

---
#### simple.html
```css
        @font-face {
            font-family: 'BriosoProItalic';
            src: url('/static/fonts/BriosoProItalic.otf') format('opentype');
        }
        :root{
            background-color: antiquewhite;
            font-family: 'BriosoProItalic';
        }
```
#### setting.py
```python
STATIC_ROOT = "static"
```

#### run
```
./manage.py collectstatic
```
