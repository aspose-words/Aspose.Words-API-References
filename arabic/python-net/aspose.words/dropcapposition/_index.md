---
title: DropCapPosition enumeration
linktitle: DropCapPosition enumeration
articleTitle: DropCapPosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.DropCapPosition enumeration. Specifies the position for a drop cap text."
type: docs
weight: 350
url: /ar/python-net/aspose.words/dropcapposition/
---

## DropCapPosition enumeration

Specifies the position for a drop cap text.


### Members

| Name | Description |
| --- | --- |
| NONE | The paragraph does not have a drop cap. |
| NORMAL | The drop cap is positioned inside the text margin on the anchor paragraph. |
| MARGIN | The drop cap is positioned outside the text margin on the anchor paragraph. |

### Examples

Shows how to create a drop cap.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أدرج فقرة واحدة بحرف كبير يبدأ به النص في الفقرتين الثانية والثالثة.
builder.font.size = 54
builder.writeln('L')
builder.font.size = 18
builder.writeln('orem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ')
builder.writeln('Ut enim ad minim veniam, quis nostrud exercitation ' + 'ullamco laboris nisi ut aliquip ex ea commodo consequat.')
# حاليًا، ستظهر الفقرتان الثانية والثالثة تحت الفقرة الأولى.
# يمكننا تحويل الفقرة الأولى إلى حرف أول كبير (Drop Cap) للفقرتين الأخريين عبر كائن "ParagraphFormat" الخاص بها.
# عيّن خاصية "DropCapPosition" إلى "DropCapPosition.Margin" لوضع الحرف الأول الكبير
# خارج هامش الصفحة الأيسر إذا كان نصنا من اليسار إلى اليمين.
# عيّن خاصية "DropCapPosition" إلى "DropCapPosition.Normal" لوضع الحرف الأول الكبير داخل هوامش الصفحة
# وللف النص المتبقي حوله.
# "DropCapPosition.None" هو الحالة الافتراضية لجميع الفقرات.
format = doc.first_section.body.first_paragraph.paragraph_format
format.drop_cap_position = drop_cap_position
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.DropCap.docx')
```

### See Also

* module [aspose.words](../)

