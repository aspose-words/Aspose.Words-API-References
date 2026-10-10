---
title: "Méthode Aspose::Words::DocumentBuilder::InsertDocumentInline"
linktitle: "InsertDocumentInline"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBuilder::InsertDocumentInline. Insère un document en ligne à la position du curseur en C++."
type: docs
weight: 33500
url: /fr/cpp/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder::InsertDocumentInline method


Insère un document en ligne à la position du curseur.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBuilder::InsertDocumentInline(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Document source à insérer. |
| importFormatMode | Aspose::Words::ImportFormatMode | Spécifie comment fusionner le formatage de style qui entre en conflit. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Permet de spécifier des options qui affectent le formatage d'un document résultat. |

### ReturnValue

Premier nœud du contenu inséré.
## Remarques


Cette méthode imite le comportement de MS Word, comme si CTRL+'A' (sélectionner tout le contenu) était pressé, puis CTRL+'C' (copier la sélection dans le tampon) dans un document, puis CTRL+'V' (insérer le contenu du tampon) dans un autre document.

Contrairement à [InsertDocument()](../), cette méthode déplace le contenu du paragraphe du document de destination, avant lequel le document source est inséré, dans le dernier paragraphe du document source inséré. En fait, cela signifie que le saut de paragraphe du dernier paragraphe inséré est supprimé.

Remarque: si le dernier nœud du document source n’est pas un paragraphe, aucune action ne sera effectuée.

## Exemples



Montre comment insérer un document en ligne à la position du curseur.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::DocumentBuilder>();
srcDoc->Write(u"[src content]");

// Créer le document de destination.
auto dstDoc = System::MakeObject<Aspose::Words::DocumentBuilder>();
dstDoc->Write(u"Before ");
dstDoc->InsertNode(System::MakeObject<Aspose::Words::BookmarkStart>(dstDoc->get_Document(), u"src_place"));
dstDoc->InsertNode(System::MakeObject<Aspose::Words::BookmarkEnd>(dstDoc->get_Document(), u"src_place"));
dstDoc->Write(u" after");

ASSERT_EQ(u"Before  after", dstDoc->get_Document()->GetText().TrimEnd(System::MakeObject<System::Array<char16_t>>(0)));

// Insérer le document source dans la destination en ligne.
dstDoc->MoveToBookmark(u"src_place");
dstDoc->InsertDocumentInline(srcDoc->get_Document(), Aspose::Words::ImportFormatMode::UseDestinationStyles, System::MakeObject<Aspose::Words::ImportFormatOptions>());

ASSERT_EQ(u"Before [src content] after", dstDoc->get_Document()->GetText().TrimEnd(System::MakeObject<System::Array<char16_t>>(0)));
```

## Voir aussi

* Class [Node](../../node/)
* Class [Document](../../document/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
