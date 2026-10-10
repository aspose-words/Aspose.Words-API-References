---
title: "Méthode Aspose::Words::DocumentBuilder::InsertOleObject"
linktitle: "InsertOleObject"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBuilder::InsertOleObject. Insère un objet OLE intégré à partir d'un flux dans le document en C++."
type: docs
weight: 41000
url: /fr/cpp/aspose.words/documentbuilder/insertoleobject/
---
## DocumentBuilder::InsertOleObject(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Insère un objet OLE incorporé à partir d'un flux dans le document.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Flux contenant les données de l'application. |
| progId | const System::String\& | Identifiant programmatique de l'objet OLE. |
| asIcon | bool | Spécifie le mode Icône ou Normal de l'objet OLE à insérer. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Présentation d'image de l'objet OLE. Si la valeur est **null**, Aspose.Words utilisera l'une des images prédéfinies. |

### ReturnValue

Nœud de forme contenant l'objet Ole et inséré à la position actuelle du Builder.

## Exemples



Montre comment utiliser le constructeur de document pour intégrer des objets OLE dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérer une feuille de calcul Microsoft Excel depuis le système de fichiers local
// dans le document tout en conservant son apparence par défaut.
{
    System::SharedPtr<System::IO::Stream> spreadsheetStream = System::IO::File::Open(get_MyDir() + u"Spreadsheet.xlsx", System::IO::FileMode::Open);
    builder->Writeln(u"Spreadsheet Ole object:");
    // Si 'presentation' est omis et que 'asIcon' est défini, cette méthode surchargée sélectionne
    // l'icône selon 'progId' et utilise la légende d'icône prédéfinie.
    builder->InsertOleObject(spreadsheetStream, u"OleObject.xlsx", false, nullptr);
}

// Insérer une présentation Microsoft PowerPoint en tant qu'objet OLE.
// Cette fois, il aura une image téléchargée depuis le web pour une icône.
{
    System::SharedPtr<System::IO::Stream> powerpointStream = System::IO::File::Open(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    System::ArrayPtr<uint8_t> imgBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

    {
        auto imageStream = System::MakeObject<System::IO::MemoryStream>(imgBytes);
        builder->InsertParagraph();
        builder->Writeln(u"Powerpoint Ole object:");
        builder->InsertOleObject(powerpointStream, u"OleObject.pptx", true, imageStream);
    }
}

// Double-cliquez sur ces objets dans Microsoft Word pour ouvrir
// les fichiers liés en utilisant leurs applications respectives.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjects.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Insère un objet OLE incorporé ou lié à partir d'un fichier dans le document. Détecte le type d'objet OLE à l'aide de l'extension du fichier.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Chemin complet du fichier. |
| isLinked | bool | Si **true**, alors l'objet OLE lié est inséré, sinon l'objet OLE incorporé est inséré. |
| asIcon | bool | Spécifie le mode Icône ou Normal de l'objet OLE à insérer. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Présentation d'image de l'objet OLE. Si la valeur est **null**, Aspose.Words utilisera l'une des images prédéfinies. |

### ReturnValue

Nœud de forme contenant l'objet Ole et inséré à la position actuelle du Builder.

## Exemples



Montre comment insérer un objet OLE dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Les objets OLE sont des liens vers des fichiers de notre système de fichiers local qui peuvent être ouverts par d'autres applications installées.
// Un double-clic sur ces formes lancera l'application, puis l'utilisera pour ouvrir l'objet lié.
// Il existe trois manières d'utiliser la méthode InsertOleObject pour insérer ces formes et configurer leur apparence.
// 1 -  Image provenant du système de fichiers local :
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // Si 'presentation' est omis et que 'asIcon' est défini, cette méthode surchargée sélectionne
    // l'icône selon l'extension du fichier et utilise le nom de fichier comme légende de l'icône.
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// Si 'presentation' est omis et que 'asIcon' est défini, cette méthode surchargée sélectionne
// l'icône selon 'progId' et utilise le nom de fichier comme légende de l'icône.
// 2 -  Icône basée sur l'application qui ouvrira l'objet :
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// Si 'iconFile' et 'iconCaption' sont omis, cette méthode surchargée sélectionne
// l'icône selon 'progId' et utilise la légende d'icône prédéfinie.
// 3 -  Icône image de 32 x 32 pixels ou moins provenant du système de fichiers local, avec une légende personnalisée :
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Insère un objet OLE incorporé ou lié à partir d'un fichier dans le document. Détecte le type d'objet OLE à l'aide du paramètre progID fourni.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, const System::String &progId, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Chemin complet du fichier. |
| progId | const System::String\& | ProgId de l'objet OLE. |
| isLinked | bool | Si **true**, alors l'objet OLE lié est inséré, sinon l'objet OLE incorporé est inséré. |
| asIcon | bool | Spécifie le mode Icône ou Normal de l'objet OLE à insérer. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Présentation d'image de l'objet OLE. Si la valeur est **null**, Aspose.Words utilisera l'une des images prédéfinies. |

### ReturnValue

Nœud de forme contenant l'objet Ole et inséré à la position actuelle du Builder.

## Exemples



Montre comment insérer un objet OLE dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Les objets OLE sont des liens vers des fichiers de notre système de fichiers local qui peuvent être ouverts par d'autres applications installées.
// Un double-clic sur ces formes lancera l'application, puis l'utilisera pour ouvrir l'objet lié.
// Il existe trois manières d'utiliser la méthode InsertOleObject pour insérer ces formes et configurer leur apparence.
// 1 -  Image provenant du système de fichiers local :
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // Si 'presentation' est omis et que 'asIcon' est défini, cette méthode surchargée sélectionne
    // l'icône selon l'extension du fichier et utilise le nom de fichier comme légende de l'icône.
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// Si 'presentation' est omis et que 'asIcon' est défini, cette méthode surchargée sélectionne
// l'icône selon 'progId' et utilise le nom de fichier comme légende de l'icône.
// 2 -  Icône basée sur l'application qui ouvrira l'objet :
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// Si 'iconFile' et 'iconCaption' sont omis, cette méthode surchargée sélectionne
// l'icône selon 'progId' et utilise la légende d'icône prédéfinie.
// 3 -  Icône image de 32 x 32 pixels ou moins provenant du système de fichiers local, avec une légende personnalisée :
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(std::basic_istream<CharType, Traits> &stream, System::String progId, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, System::String progId, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
