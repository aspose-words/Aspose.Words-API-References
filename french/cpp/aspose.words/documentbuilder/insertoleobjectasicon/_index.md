---
title: "Méthode Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon"
linktitle: "InsertOleObjectAsIcon"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon. Insère un objet OLE intégré sous forme d'icône à partir d'un flux dans le document. Permet de spécifier le fichier d'icône et la légende. Détecte le type d'objet OLE en utilisant le paramètre progID fourni en C++."
type: docs
weight: 42000
url: /fr/cpp/aspose.words/documentbuilder/insertoleobjectasicon/
---
## DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) method


Insère un objet OLE incorporé sous forme d'icône à partir d'un flux dans le document. Permet de spécifier le fichier d'icône et la légende. Détecte le type d'objet OLE à l'aide du paramètre progID fourni.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, const System::String &iconFile, const System::String &iconCaption)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Flux contenant les données de l'application. |
| progId | const System::String\& | ProgId de l'objet OLE. |
| iconFile | const System::String\& | Chemin complet du fichier ICO. Si la valeur est **null**, Aspose.Words utilisera une image prédéfinie. |
| iconCaption | const System::String\& | Légende de l'icône. Si la valeur est **null**, Aspose.Words utilisera une légende d'icône prédéfinie. |

### ReturnValue

Nœud de forme contenant l'objet Ole et inséré à la position actuelle du Builder.

## Exemples



Montre comment insérer un objet OLE incorporé ou lié sous forme d'icône dans le document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Si 'iconFile' et 'iconCaption' sont omis, cette méthode surchargée sélectionne
// l'icône selon 'progId' et utilise le nom de fichier comme légende de l'icône.
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // Si 'iconFile' et 'iconCaption' sont omis, cette méthode surchargée sélectionne
    // l'icône selon l'extension du fichier et utilise le nom de fichier comme légende de l'icône.
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, bool, const System::String\&, const System::String\&) method


Insère un objet OLE incorporé ou lié sous forme d'icône dans le document. Permet de spécifier le fichier d'icône et la légende. Détecte le type d'objet OLE à l'aide de l'extension du fichier.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Chemin complet du fichier. |
| isLinked | bool | Si **true**, alors l'objet OLE lié est inséré, sinon l'objet OLE incorporé est inséré. |
| iconFile | const System::String\& | Chemin complet du fichier ICO. Si la valeur est **null**, Aspose.Words utilisera une image prédéfinie. |
| iconCaption | const System::String\& | Légende de l'icône. Si la valeur est **null**, Aspose.Words utilisera le nom du fichier. |

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
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) method


Insère un objet OLE incorporé ou lié sous forme d'icône dans le document. Permet de spécifier le fichier d'icône et la légende. Détecte le type d'objet OLE à l'aide du paramètre progID fourni.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, const System::String &progId, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Chemin complet du fichier. |
| progId | const System::String\& | ProgId de l'objet OLE. |
| isLinked | bool | Si **true**, alors l'objet OLE lié est inséré, sinon l'objet OLE incorporé est inséré. |
| iconFile | const System::String\& | Chemin complet du fichier ICO. Si la valeur est **null**, Aspose.Words utilisera une image prédéfinie. |
| iconCaption | const System::String\& | Légende de l'icône. Si la valeur est **null**, Aspose.Words utilisera le nom du fichier. |

### ReturnValue

Nœud de forme contenant l'objet Ole et inséré à la position actuelle du Builder.

## Exemples



Montre comment insérer un objet OLE incorporé ou lié sous forme d'icône dans le document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Si 'iconFile' et 'iconCaption' sont omis, cette méthode surchargée sélectionne
// l'icône selon 'progId' et utilise le nom de fichier comme légende de l'icône.
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // Si 'iconFile' et 'iconCaption' sont omis, cette méthode surchargée sélectionne
    // l'icône selon l'extension du fichier et utilise le nom de fichier comme légende de l'icône.
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream<CharType, Traits> &stream, System::String progId, System::String iconFile, System::String iconCaption)
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
