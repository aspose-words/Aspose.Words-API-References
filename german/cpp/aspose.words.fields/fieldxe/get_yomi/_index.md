---
title: "Aspose::Words::Fields::FieldXE::get_Yomi Methode"
linktitle: "get_Yomi"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldXE::get_Yomi Methode. Ermittelt oder legt das Yomi (erstes phonetisches Zeichen zum Sortieren von Indexeinträgen) für den Indexeintrag in C++ fest."
type: docs
weight: 8000
url: /de/cpp/aspose.words.fields/fieldxe/get_yomi/
---
## FieldXE::get_Yomi method


Liest oder setzt das Yomi (erstes phonetische Zeichen zum Sortieren von Indizes) für den Indexeintrag.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_Yomi()
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

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
