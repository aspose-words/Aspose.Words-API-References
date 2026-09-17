---
title: "Aspose::Words::Paragraph::get_IsInsertRevision méthode"
linktitle: "get_IsInsertRevision"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Paragraph::get_IsInsertRevision méthode. Retourne vrai si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words/paragraph/get_isinsertrevision/
---
## Paragraph::get_IsInsertRevision method


Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé.

```cpp
bool Aspose::Words::Paragraph::get_IsInsertRevision()
```


## Exemples



Montre comment travailler avec des paragraphes de révision.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();
System::SharedPtr<Aspose::Words::Paragraph> para = body->get_FirstParagraph();

para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Paragraph 1. "));
body->AppendParagraph(u"Paragraph 2. ");
body->AppendParagraph(u"Paragraph 3. ");

// Les paragraphes ci‑dessus ne sont pas des révisions.
// Les paragraphes que nous ajoutons après le démarrage du suivi des modifications seront enregistrés comme des révisions "Insert".
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

para = body->AppendParagraph(u"Paragraph 4. ");

ASSERT_TRUE(para->get_IsInsertRevision());

// Les paragraphes que nous supprimons après le démarrage du suivi des modifications seront enregistrés comme des révisions "Delete".
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = body->get_Paragraphs();

ASSERT_EQ(4, paragraphs->get_Count());

para = paragraphs->idx_get(2);
para->Remove();

// Ces paragraphes resteront jusqu'à ce que nous acceptions ou rejetions la révision de suppression.
// Accepter la révision supprimera le paragraphe définitivement,
// et rejeter la révision le laissera dans le document comme si nous ne l'avions jamais supprimé.
ASSERT_EQ(4, paragraphs->get_Count());
ASSERT_TRUE(para->get_IsDeleteRevision());

// Acceptez la révision, puis vérifiez que le paragraphe a disparu.
doc->AcceptAllRevisions();

ASSERT_EQ(3, paragraphs->get_Count());
ASSERT_EQ(0, para->get_Count());
ASSERT_EQ(System::String(u"Paragraph 1. \r") + u"Paragraph 2. \r" + u"Paragraph 4.", doc->GetText().Trim());
```

## Voir aussi

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
