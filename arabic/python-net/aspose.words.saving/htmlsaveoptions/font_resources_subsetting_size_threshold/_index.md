---
title: HtmlSaveOptions.font_resources_subsetting_size_threshold property
linktitle: font_resources_subsetting_size_threshold property
articleTitle: font_resources_subsetting_size_threshold property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.font_resources_subsetting_size_threshold property. Controls which font resources need subsetting when saving to HTML, MHTML or EPUB"
type: docs
weight: 290
url: /ar/python-net/aspose.words.saving/htmlsaveoptions/font_resources_subsetting_size_threshold/
---

## HtmlSaveOptions.font_resources_subsetting_size_threshold property

Controls which font resources need subsetting when saving to HTML, MHTML or EPUB.
Default is ``0``.



```python
@property
def font_resources_subsetting_size_threshold(self) -> int:
    ...

@font_resources_subsetting_size_threshold.setter
def font_resources_subsetting_size_threshold(self, value: int):
    ...

```

### Remarks

[HtmlSaveOptions.export_font_resources](../export_font_resources/) allows exporting fonts as subsidiary files or as parts of the output
package. If the document uses many fonts, especially with large number of glyphs, then output size can grow
significantly. Font subsetting reduces the size of the exported font resource by filtering out glyphs that
are not used by the current document.

Font subsetting works as follows:


* By default, all exported fonts are subsetted.
  
* Setting [HtmlSaveOptions.font_resources_subsetting_size_threshold](./) to a positive value
  instructs Aspose.Words to subset fonts which file size is larger than the specified value.
  
* Setting the property to int.MaxValue C# constant
  suppresses font subsetting.
  
**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable
font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not
allow web downloading of their fonts in any form. License agreements that cover some fonts specifically note that usage via **@font-face** rules
in CSS style sheets is not allowed. Font subsetting can also violate license terms.





### Examples

Shows how to work with font subsetting.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Times New Roman'
builder.writeln('Hello world!')
builder.font.name = 'Courier New'
builder.writeln('Hello world!')
# عند حفظ المستند إلى HTML، يمكننا تمرير كائن SaveOptions لتكوين تقليل الخطوط.
# افترض أننا ضبطنا علامة "export_font_resources" إلى "True" وأيضًا سمينا مجلدًا في خاصية "fonts_folder".
# في هذه الحالة، ستقوم عملية الحفظ بإنشاء ذلك المجلد ووضع ملف .ttf داخله
# ذلك المجلد لكل خط يستخدمه مستندنا.
# كل ملف .ttf سيحتوي على مجموعة الأحرف الكاملة لذلك الخط،
# مما قد ينتج عنه ملف كبير جدًا يرافق المستند.
# عند تطبيق التقسيم الجزئي على الخط، ستحتوي البيانات الخام المصدرة له فقط على الأحرف التي يستخدمها المستند
# بدلاً من مجموعة الأحرف الكاملة. إذا كان النص في مستندنا يستخدم فقط جزءًا صغيرًا من مجموعة الأحرف الخاصة بالخط
# مجموعة الأحرف، فإن التقسيم الجزئي سيقلل بشكل كبير من حجم مستنداتنا الناتجة.
# يمكننا استخدام الخاصية "font_resources_subsetting_size_threshold" لتحديد حجم ملف .ttf، بالبايت.
# إذا أنشأ الخط المصدّر ملفًا بحجم أكبر من ذلك، فستقوم عملية الحفظ بتطبيق التقسيم الجزئي على ذلك الخط.
# ضبط الحد عند 0 يطبق التقسيم الجزئي على جميع الخطوط،
# وتعيينه إلى "2**31 - 1" يعطل التقسيم الجزئي فعليًا.
fonts_folder = ARTIFACTS_DIR + 'HtmlSaveOptions.font_subsetting.fonts'
if os.path.exists(fonts_folder):
    shutil.rmtree(fonts_folder)
options = aw.saving.HtmlSaveOptions()
options.export_font_resources = True
options.fonts_folder = fonts_folder
options.font_resources_subsetting_size_threshold = font_resources_subsetting_size_threshold
doc.save(ARTIFACTS_DIR + 'HtmlSaveOptions.font_subsetting.html', options)
font_file_names = glob.glob(fonts_folder + '/*.ttf')
self.assertEqual(3, len(font_file_names))
for filename in font_file_names:
    # بشكل افتراضي، ستكون ملفات .ttf لكل من خطوطنا الثلاثة أكبر من 700 ميغابايت.
    # سيقلل التقسيم الجزئي جميعها إلى أقل من 30 ميغابايت.
    font_file_size = os.path.getsize(filename)
    self.assertTrue(font_file_size > 700000 or font_file_size < 30000)
    self.assertTrue(max(font_resources_subsetting_size_threshold, 30000) > font_file_size)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.export_font_resources](../export_font_resources/)

