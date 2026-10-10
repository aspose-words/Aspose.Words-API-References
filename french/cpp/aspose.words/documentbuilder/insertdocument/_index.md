---
title: "Aspose::Words::DocumentBuilder::InsertDocument method"
linktitle: "InsertDocument"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::InsertDocument méthode. Insère un document à la position du curseur en C++."
type: docs
weight: 33000
url: /fr/cpp/aspose.words/documentbuilder/insertdocument/
---
## DocumentBuilder::InsertDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) method


Insère un document à la position du curseur.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBuilder::InsertDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Document source à insérer. |
| importFormatMode | Aspose::Words::ImportFormatMode | Spécifie comment fusionner le formatage de style qui entre en conflit. |

### ReturnValue

Premier nœud du contenu inséré.

## Exemples



Montre comment insérer un document dans un autre document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

auto docToInsert = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Formatted elements.docx");

builder->InsertDocument(docToInsert, Aspose::Words::ImportFormatMode::KeepSourceFormatting);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertDocument.docx");
```

## Voir aussi

* Class [Node](../../node/)
* Class [Document](../../document/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


Insère un document à la position du curseur.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBuilder::InsertDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Document source à insérer. |
| importFormatMode | Aspose::Words::ImportFormatMode | Spécifie comment fusionner le formatage de style qui entre en conflit. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Permet de spécifier des options qui affectent le formatage d'un document résultat. |

### ReturnValue

Premier nœud du contenu inséré.

## Exemples



Montre comment résoudre les styles en double lors de l'insertion de documents.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

System::SharedPtr<Aspose::Words::Style> myStyle = builder->get_Document()->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

// Clonez le document et modifiez le style "MyStyle" du clone, afin qu'il ait une couleur différente de celle de l'original.
// Si nous insérons le clone dans le document original, les deux styles portant le même nom provoqueront un conflit.
System::SharedPtr<Aspose::Words::Document> srcDoc = dstDoc->Clone();
srcDoc->get_Styles()->idx_get(u"MyStyle")->get_Font()->set_Color(System::Drawing::Color::get_Red());

// Lorsque nous activons SmartStyleBehavior et utilisons le mode d'importation KeepSourceFormatting,
// Aspose.Words résoudra les conflits de styles en convertissant les styles du document source.
// avec les mêmes noms que les styles de destination en attributs de paragraphe directs.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_SmartStyleBehavior(true);

builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.SmartStyleBehavior.docx");
```

## Voir aussi

* Class [Node](../../node/)
* Class [Document](../../document/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
