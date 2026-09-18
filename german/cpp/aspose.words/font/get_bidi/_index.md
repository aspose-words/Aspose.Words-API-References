---
title: "Aspose::Words::Font::get_Bidi Methode"
linktitle: "get_Bidi"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Bidi Methode. Gibt an, ob der Inhalt dieses Laufs rechts-nach-links-Merkmale aufweisen soll in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words/font/get_bidi/
---
## Font::get_Bidi method


Gibt an, ob der Inhalt dieses Laufs rechts-nach-links-Eigenschaften haben soll.

```cpp
bool Aspose::Words::Font::get_Bidi()
```

## Hinweise


Diese Eigenschaft darf, wenn sie aktiviert ist, nicht mit stark links-nach-rechts-Text verwendet werden. Jegliches Verhalten unter dieser Bedingung ist nicht spezifiziert. Diese Eigenschaft darf, wenn sie deaktiviert ist, nicht mit stark rechts-nach-links-Text verwendet werden. Jegliches Verhalten unter dieser Bedingung ist nicht spezifiziert.

Wenn der Inhalt dieses Laufs angezeigt wird, sollen alle Zeichen für Formatierungszwecke als Zeichen komplexer Schriften behandelt werden. Das bedeutet, dass [BoldBi](../get_boldbi/), [ItalicBi](../get_italicbi/), [SizeBi](../get_sizebi/) und ein entsprechender Schriftname beim Rendern dieses Laufs verwendet werden.

Außerdem wirkt diese Eigenschaft, wenn der Inhalt dieses Laufs angezeigt wird, als Rechts-nach-Links-Überschreibung für Zeichen, die als \"weak types\" und \"neutral types\" klassifiziert sind.

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
