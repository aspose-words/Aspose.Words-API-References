---
title: ChmLoadOptions
linktitle: ChmLoadOptions
articleTitle: ChmLoadOptions
second_title: Aspose.Words لـ .NET
description: اكتشف مُنشئ ChmLoadOptions لتهيئة سلسة. عيّن القيم الافتراضية بسهولة، وحسّن أداء تطبيقك اليوم!
type: docs
weight: 10
url: /ar/net/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions constructor

يقوم بتهيئة مثيل جديد لهذه الفئة بالقيم الافتراضية.

```csharp
public ChmLoadOptions()
```

## أمثلة

يوضح كيفية حل عناوين URL مثل "ms-its:myfile.chm::/index.htm".

```csharp
// تحتوي مستندنا على عناوين URL مثل "ms-its:amhelp.chm::....htm"، ولكن لها اسم مختلف،
// لذلك فإن روابط الملف لا تعمل بعد حفظه في HTML.
// نحتاج إلى تحديد اسم الملف الأصلي في 'ChmLoadOptions' لتجنب هذا السلوك.
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### أنظر أيضا

* class [ChmLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
