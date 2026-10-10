---
title: "Aspose::Words::NodeImporter::NodeImporter constructeur"
linktitle: "NodeImporter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::NodeImporter::NodeImporter constructeur. Initialise une nouvelle instance de la classe NodeImporter en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter::NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) constructor


Initialise une nouvelle instance de la classe [NodeImporter](../).

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Le document source. |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Le document de destination qui sera le propriétaire des nœuds importés. |
| importFormatMode | Aspose::Words::ImportFormatMode | Spécifie comment fusionner le formatage de style qui entre en conflit. |

## Voir aussi

* Class [DocumentBase](../../documentbase/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## NodeImporter::NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) constructor


Initialise une nouvelle instance de la classe [NodeImporter](../).

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Le document source. |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Le document de destination qui sera le propriétaire des nœuds importés. |
| importFormatMode | Aspose::Words::ImportFormatMode | Spécifie comment fusionner le formatage de style qui entre en conflit. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Spécifie diverses options pour formater le nœud importé. |

## Exemples



Montre comment résoudre un conflit lors de l'importation de documents contenant des listes avec le même identifiant de définition de liste.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - destination.docx");

// Définissez la propriété "KeepSourceNumbering" sur "true" pour appliquer un ID de définition de liste différent
// aux styles identiques que Aspose.Words importe dans les documents de destination.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(true);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, importFormatOptions);
dstDoc->UpdateListLabels();
```


Montre comment résoudre les conflits de numérotation de listes dans les documents source et destination.
```cpp
// Ouvrez un document avec un schéma de numérotation de liste personnalisé, puis clonez-le.
// Comme les deux ont le même format de numérotation, les formats entreront en conflit si nous importons un document dans l'autre.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom list numbering.docx");
System::SharedPtr<Aspose::Words::Document> dstDoc = srcDoc->Clone();

// Lorsque nous importons le clone du document dans l'original puis l'ajoutons,
// alors les deux listes avec le même format de liste se fusionneront.
// Si nous définissons le drapeau "KeepSourceNumbering" sur "false", alors la liste du clone du document
// que nous ajoutons à l'original continuera la numérotation de la liste à laquelle nous l'ajoutons.
// Cela fusionnera effectivement les deux listes en une seule.
// Si nous définissons le drapeau "KeepSourceNumbering" sur "true", alors le clone du document
// la liste conservera sa numérotation originale, faisant apparaître les deux listes comme des listes séparées.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(keepSourceNumbering);

auto importer = System::MakeObject<Aspose::Words::NodeImporter>(srcDoc, dstDoc, Aspose::Words::ImportFormatMode::KeepDifferentStyles, importFormatOptions);
for (auto&& paragraph : System::IterateOver<Aspose::Words::Paragraph>(srcDoc->get_FirstSection()->get_Body()->get_Paragraphs()))
{
    System::SharedPtr<Aspose::Words::Node> importedNode = importer->ImportNode(paragraph, true);
    dstDoc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Node>>(importedNode);
}

dstDoc->UpdateListLabels();

if (keepSourceNumbering)
{
    ASSERT_EQ(System::String(u"6. Item 1\r\n") + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4\r\n" + u"6. Item 1\r\n" + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4", dstDoc->get_FirstSection()->get_Body()->ToString(Aspose::Words::SaveFormat::Text).Trim());
}
else
{
    ASSERT_EQ(System::String(u"6. Item 1\r\n") + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4\r\n" + u"10. Item 1\r\n" + u"11. Item 2 \r\n" + u"12. Item 3\r\n" + u"13. Item 4", dstDoc->get_FirstSection()->get_Body()->ToString(Aspose::Words::SaveFormat::Text).Trim());
}
```

## Voir aussi

* Class [DocumentBase](../../documentbase/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
