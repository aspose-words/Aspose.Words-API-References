---
title: Font.clear_formatting method
linktitle: clear_formatting method
articleTitle: clear_formatting method
second_title: Aspose.Words for Python
description: "Font.clear_formatting method. Resets to default font formatting."
type: docs
weight: 560
url: /tr/python-net/aspose.words/font/clear_formatting/
---

## clear_formatting() {#default}

Resets to default font formatting.


```python
def clear_formatting(self):
    ...
```

### Remarks

Removes all font formatting specified explicitly on the object from which
[Font](../) was obtained so the font formatting will be inherited from
the appropriate parent.




### Examples

Shows how to insert a hyperlink field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('For more information, please visit the ')
# Bir köprü ekleyin ve özel biçimlendirme ile vurgulayın.
# Köprü, URL'de belirtilen konuma götürecek tıklanabilir bir metin parçası olacaktır.
builder.font.color = aspose.pydrawing.Color.blue
builder.font.underline = aw.Underline.SINGLE
builder.insert_hyperlink('Google website', 'https://www.google.com', False)
builder.font.clear_formatting()
builder.writeln('.')
# Microsoft Word'de metindeki bağlantıya Ctrl + sol tıklama, yeni bir web tarayıcı penceresi aracılığıyla URL'ye götürür.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertHyperlink.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

