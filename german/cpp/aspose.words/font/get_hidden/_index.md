---
title: "Aspose::Words::Font::get_Hidden Methode"
linktitle: "get_Hidden"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Hidden Methode. Wahr, wenn die Schriftart als versteckter Text in C++ formatiert ist."
type: docs
weight: 16000
url: /de/cpp/aspose.words/font/get_hidden/
---
## Font::get_Hidden method


True, wenn die Schrift als versteckter Text formatiert ist.

```cpp
bool Aspose::Words::Font::get_Hidden()
```


## Beispiele



Zeigt, wie man einen Lauf versteckten Textes erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Wenn das Hidden-Flag auf true gesetzt ist, wird jeder Text, den wir mit diesem Font-Objekt erstellen, im Dokument unsichtbar sein.
// Wir werden keinen versteckten Text sehen oder hervorheben, es sei denn, wir aktivieren die Option "Hidden text".
// gefunden in Microsoft Word über "Datei" -> "Optionen" -> "Anzeige". Der Text wird weiterhin vorhanden sein,
// und wir werden in der Lage sein, auf diesen Text programmgesteuert zuzugreifen.
// Es wird nicht empfohlen, diese Methode zu verwenden, um sensible Informationen zu verbergen.
builder->get_Font()->set_Hidden(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text will not be visible in the document.");

doc->Save(get_ArtifactsDir() + u"Font.Hidden.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
