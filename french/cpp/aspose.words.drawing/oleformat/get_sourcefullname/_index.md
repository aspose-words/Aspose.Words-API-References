---
title: "Aspose::Words::Drawing::OleFormat::get_SourceFullName méthode"
linktitle: "get_SourceFullName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::OleFormat::get_SourceFullName méthode. Obtient ou définit le chemin et le nom du fichier source pour l'objet OLE lié en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.drawing/oleformat/get_sourcefullname/
---
## OleFormat::get_SourceFullName method


Obtient ou définit le chemin et le nom du fichier source pour l'objet OLE lié.

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_SourceFullName()
```

## Remarques


La valeur par défaut est une chaîne vide.

Si [SourceFullName](./) n'est pas une chaîne vide, l'objet OLE est lié.

## Exemples



Montre comment insérer des objets OLE liés et non liés.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Intégrez un dessin Microsoft Visio dans le document en tant qu'objet OLE.
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", false, false, nullptr);

// Insérez un lien vers le fichier dans le système de fichiers local et affichez-le sous forme d'icône.
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", true, true, nullptr);

// L'insertion d'objets OLE crée des formes qui stockent ces objets.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());
ASSERT_EQ(2, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::OleObject;
}))));

// Si une forme contient un objet OLE, elle aura une propriété "OleFormat" valide,
// que nous pouvons utiliser pour vérifier certains aspects de la forme.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shapes[0]->get_OleFormat();

ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLink());
ASPOSE_ASSERT_EQ(false, oleFormat->get_OleIcon());

oleFormat = shapes[1]->get_OleFormat();

ASPOSE_ASSERT_EQ(true, oleFormat->get_IsLink());
ASPOSE_ASSERT_EQ(true, oleFormat->get_OleIcon());

ASSERT_TRUE(oleFormat->get_SourceFullName().EndsWith(System::String(u"Images") + System::IO::Path::DirectorySeparatorChar + u"Microsoft Visio drawing.vsd"));
ASSERT_EQ(u"", oleFormat->get_SourceItem());

ASSERT_EQ(u"Microsoft Visio drawing.vsd", oleFormat->get_IconCaption());

doc->Save(get_ArtifactsDir() + u"Shape.OleLinks.docx");

// Si l'objet contient des données OLE, nous pouvons y accéder à l'aide d'un flux.
{
    System::SharedPtr<System::IO::MemoryStream> stream = oleFormat->GetOleEntry(u"\x0001" u"CompObj");
    System::ArrayPtr<uint8_t> oleEntryBytes = stream->ToArray();
    ASSERT_EQ(76, oleEntryBytes->get_Length());
}
```

## Voir aussi

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
