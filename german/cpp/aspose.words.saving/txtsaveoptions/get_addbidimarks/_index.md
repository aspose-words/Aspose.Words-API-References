---
title: "Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks-Methode"
linktitle: "get_AddBidiMarks"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks-Methode. Gibt an, ob bidirektionale Markierungen vor jedem BiDi‑Lauf beim Exportieren im Nur‑Text‑Format hinzugefügt werden sollen. Der Standardwert ist false in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.saving/txtsaveoptions/get_addbidimarks/
---
## TxtSaveOptions::get_AddBidiMarks method


Gibt an, ob vor jedem BiDi‑Lauf bi‑directionale Markierungen hinzugefügt werden sollen, wenn im Klartextformat exportiert wird. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks() const
```


## Beispiele



Zeigt, wie das Unicode‑Zeichen 'RIGHT-TO-LEFT MARK' (U+200F) vor jedem bidirektionalen [Run](../../../aspose.words/run/) im Text eingefügt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Bidi(true);
builder->Writeln(u"שלום עולם!");
builder->Writeln(u"مرحبا بالعالم!");

// Erstelle ein "TxtSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie wir das Dokument in Klartext speichern.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_Encoding(System::Text::Encoding::get_Unicode());

// Setzen Sie die Eigenschaft "AddBidiMarks" auf "true", um Markierungen vor Läufen hinzuzufügen
// bei rechts‑nach‑links‑Text, um den Umstand anzuzeigen.
// Setzen Sie die Eigenschaft "AddBidiMarks" auf "false", um alles von links nach rechts zu schreiben
// und rechts‑nach‑links‑Läufe gleichermaßen, ohne etwas anzugeben, welches welches ist.
saveOptions->set_AddBidiMarks(addBidiMarks);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.AddBidiMarks.txt", saveOptions);

System::String docText = System::Text::Encoding::get_Unicode()->GetString(System::IO::File::ReadAllBytes(get_ArtifactsDir() + u"TxtSaveOptions.AddBidiMarks.txt"));

if (addBidiMarks)
{
    ASSERT_EQ(u"\ufeffHello world!‎\r\nשלום עולם!‏\r\nمرحبا بالعالم!‏\r\n\r\n", docText);
    ASSERT_TRUE(docText.Contains(u"\u200f"));
}
else
{
    ASSERT_EQ(u"\ufeffHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n", docText);
    ASSERT_FALSE(docText.Contains(u"\u200f"));
}
```

## Siehe auch

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
