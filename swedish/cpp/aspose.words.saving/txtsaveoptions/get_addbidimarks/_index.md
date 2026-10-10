---
title: "Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks metod"
linktitle: "get_AddBidiMarks"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks‑metod. Anger om bi‑direktionella markeringar ska läggas till före varje BiDi‑körning vid export i vanligt textformat. Standardvärdet är falskt i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.saving/txtsaveoptions/get_addbidimarks/
---
## TxtSaveOptions::get_AddBidiMarks method


Anger om bi‑riktade markeringar ska läggas till före varje BiDi‑sekvens vid export i vanligt textformat. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks() const
```


## Exempel



Visar hur man infogar Unicode‑tecknet 'RIGHT-TO-LEFT MARK' (U+200F) före varje bi‑direktionell [Run](../../../aspose.words/run/) i text.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Bidi(true);
builder->Writeln(u"שלום עולם!");
builder->Writeln(u"مرحبا بالعالم!");

// Skapa ett \"TxtSaveOptions\"-objekt, som vi kan skicka till dokumentets \"Save\"-metod
// för att ändra hur vi sparar dokumentet som ren text.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_Encoding(System::Text::Encoding::get_Unicode());

// Ställ in egenskapen "AddBidiMarks" till "true" för att lägga till markeringar före körningar
// med höger‑till‑vänster‑text för att indikera detta.
// Ställ in egenskapen "AddBidiMarks" till "false" för att skriva all text från vänster till höger
// och höger‑till‑vänster‑körningar lika utan någon indikation på vilken som är vilken.
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

## Se även

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
