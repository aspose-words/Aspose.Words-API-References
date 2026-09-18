---
title: "Aspose::Words::Fields::FieldIndex::get_UseYomi Methode"
linktitle: "get_UseYomi"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldIndex::get_UseYomi Methode. Liest oder setzt, ob die Verwendung von Yomi‑Text für Indexeinträge in C++ aktiviert werden soll."
type: docs
weight: 17000
url: /de/cpp/aspose.words.fields/fieldindex/get_useyomi/
---
## FieldIndex::get_UseYomi method


Liest oder setzt, ob die Verwendung von Yomi-Text für Indexeinträge aktiviert werden soll.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_UseYomi()
```


## Beispiele



Zeigt, wie man INDEX-Feldeinträge phonetisch sortiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstelle ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
// Jeder Eintrag zeigt den Text‑Eigenschaftswert des XE-Feldes auf der linken Seite an,
// und die Seitenzahl, die das XE-Feld enthält, auf der rechten Seite.
// Der INDEX-Eintrag sammelt alle XE-Felder mit übereinstimmenden Werten in der \"Text\"-Eigenschaft.
// zu einem Eintrag, anstatt für jedes XE-Feld einen eigenen Eintrag zu erstellen.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Die INDEX-Tabelle sortiert ihre Einträge automatisch alphabetisch nach den Werten ihrer Text-Eigenschaften.
// Stellen Sie die INDEX-Tabelle so ein, dass Einträge phonetisch mit Hiragana sortiert werden.
index->set_UseYomi(sortEntriesUsingYomi);

if (sortEntriesUsingYomi)
{
    ASSERT_EQ(u" INDEX  \\y", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX ", index->GetFieldCode());
}

// Fügen Sie 4 XE-Felder ein, die als Einträge im Inhaltsverzeichnis des INDEX-Feldes angezeigt werden.
// Die \"Text\"-Eigenschaft kann die Schreibweise eines Wortes in Kanji enthalten, deren Aussprache mehrdeutig sein kann,
// während die \"Yomi\"-Version des Wortes exakt angibt, wie es mit Hiragana ausgesprochen wird.
// Wenn wir unser INDEX-Feld so einstellen, dass es Yomi verwendet, sortiert es diese Einträge
// nach dem Wert ihrer Yomi-Eigenschaften statt nach ihren Textwerten.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"愛子");
indexEntry->set_Yomi(u"あ");

ASSERT_EQ(u" XE  愛子 \\y あ", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"明美");
indexEntry->set_Yomi(u"あ");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"恵美");
indexEntry->set_Yomi(u"え");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"愛美");
indexEntry->set_Yomi(u"え");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Yomi.docx");
```

## Siehe auch

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
