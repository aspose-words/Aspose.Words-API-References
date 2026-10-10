---
title: "Aspose::Words::NumSpacing enum"
linktitle: "NumSpacing"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::NumSpacing enum. Gibt mögliche Werte an, in denen die Ziffernabstände in C++ angezeigt werden können."
type: docs
weight: 103500
url: /de/cpp/aspose.words/numspacing/
---
## NumSpacing enum


Gibt mögliche Werte an, in denen die Ziffernabstände angezeigt werden können.

```cpp
enum class NumSpacing
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Standard | 0 | Gibt an, dass Ziffern in der Standardschrift des Fonts angezeigt werden. |
| Proportional | 1 | Gibt an, dass die Formen der Ziffern, die als proportional verteilt entworfen wurden, angezeigt werden, wenn die Schriftart dies unterstützt. |
| Tabellarisch | 2 | Gibt an, dass die Formen der Ziffern, die als tabellarisch entworfen wurden, angezeigt werden, wenn die Schriftart dies unterstützt. |


## Beispiele



Zeigt, wie der Abstandstyp der Ziffer festgelegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Dieser Effekt wird nur in neueren Versionen von MS Word unterstützt.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2019);

builder->Write(u"1 ");
builder->Write(u"This is an example");

System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
if (run->get_Font()->get_NumberSpacing() == Aspose::Words::NumSpacing::Default)
{
    run->get_Font()->set_NumberSpacing(Aspose::Words::NumSpacing::Proportional);
}

doc->Save(get_ArtifactsDir() + u"Fonts.NumberSpacing.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
