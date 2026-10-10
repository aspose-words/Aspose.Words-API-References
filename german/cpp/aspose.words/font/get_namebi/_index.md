---
title: "Aspose::Words::Font::get_NameBi-Methode"
linktitle: "get_NameBi"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_NameBi-Methode. Gibt den Namen der Schriftart in einem Rechts-nach-Links-Sprachdokument in C++ zurück oder setzt ihn."
type: docs
weight: 27000
url: /de/cpp/aspose.words/font/get_namebi/
---
## Font::get_NameBi method


Gibt den Namen der Schriftart zurück oder legt ihn fest in einem Rechts-nach-Links‑Sprachdokument.

```cpp
System::String Aspose::Words::Font::get_NameBi()
```


## Beispiele



Zeigt, wie man separate Sätze von Schriftarteinstellungen für Rechts-nach-Links- und Rechts-nach-Links-Text definiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Definieren Sie einen Satz von Schriftarteinstellungen für Links-nach-Rechts-Text.
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Italic(false);
builder->get_Font()->set_Bold(false);
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// Definieren Sie einen weiteren Satz von Schriftarteinstellungen für Rechts-nach-Links-Text.
builder->get_Font()->set_NameBi(u"Andalus");
builder->get_Font()->set_SizeBi(24);
builder->get_Font()->set_ItalicBi(true);
builder->get_Font()->set_BoldBi(true);
builder->get_Font()->set_LocaleIdBi(System::MakeObject<System::Globalization::CultureInfo>(u"ar-AR", false)->get_LCID());

// Wir können das Bidi-Flag verwenden, um anzuzeigen, ob der Text, den wir hinzufügen wollen
// mit dem document builder rechts-nach-links ist. Wenn wir Text mit diesem auf true gesetzten Flag hinzufügen,
// wird er mit dem Rechts-nach-Links-Satz von Schriftarteinstellungen formatiert.
builder->get_Font()->set_Bidi(true);
builder->Write(u"مرحبًا");

// Setzen Sie das Flag auf false und fügen Sie dann Links-nach-Rechts-Text hinzu.
// Der document builder wird diese mit dem Links-nach-Rechts-Satz von Schriftarteinstellungen formatieren.
builder->get_Font()->set_Bidi(false);
builder->Write(u" Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Bidi.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
