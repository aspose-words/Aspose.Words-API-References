---
title: "Aspose::Words::Document::Document constructeur"
linktitle: "Document"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::Document constructeur. Crée un document Word vierge en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/document/document/
---
## Document::Document() constructor


Crée un document Word vierge.

```cpp
Aspose::Words::Document::Document()
```

## Remarques


Un document vierge est récupéré à partir des ressources, et par défaut, le document résultant ressemble davantage à celui créé par [Word2007](../../../aspose.words.settings/mswordversion/). Ce document vierge contient une table de polices par défaut, des styles par défaut minimaux et des styles latents.

[OptimizeFor()](../../../aspose.words.settings/compatibilityoptions/optimizefor/) method can be used to optimize the document contents as well as default Aspose.Words behavior to a particular version of MS Word.

Le format de papier du document est Letter par défaut. Si vous souhaitez modifier la mise en page, utilisez [PageSetup](../../section/get_pagesetup/).

Après la création, vous pouvez utiliser [DocumentBuilder](../../documentbuilder/) pour ajouter facilement le contenu du document.

## Exemples



Montre comment créer un document simple.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Les nouveaux objets Document sont, par défaut, fournis avec l'ensemble minimal de nœuds
// nécessaires pour commencer à ajouter du contenu tel que du texte et des formes : une Section, un Corps et un Paragraphe.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```


Montre comment créer et charger des documents.
```cpp
// Il existe deux manières de créer un objet Document en utilisant Aspose.Words.
// 1 -  Créez un document vierge :
auto doc = System::MakeObject<Aspose::Words::Document>();

// Les nouveaux objets Document sont, par défaut, fournis avec l'ensemble minimal de nœuds
// nécessaires pour commencer à ajouter du contenu tel que du texte et des formes : une Section, un Corps et un Paragraphe.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  Chargez un document qui existe dans le système de fichiers local :
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Les documents chargés contiendront des éléments que nous pouvons accéder et modifier.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// Certaines opérations qui doivent se produire lors du chargement, comme l'utilisation d'un mot de passe pour déchiffrer un document,
// peuvent être effectuées en passant un objet LoadOptions lors du chargement du document.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


Montre comment formater une séquence de texte en utilisant sa propriété de police.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&) constructor


Ouvre un document existant à partir d'un flux. Détecte automatiquement le format du fichier.

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Flux depuis lequel charger le document. |
## Remarques


Le document doit être stocké au début du flux. Le flux doit prendre en charge le positionnement aléatoire.

## Exemples



Montre comment charger un document à l'aide d'un flux.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.docx");
    auto doc = System::MakeObject<Aspose::Words::Document>(stream);

    ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());
}
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Ouvre un document existant à partir d'un flux. Permet de spécifier des options supplémentaires telles qu'un mot de passe de chiffrement.

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Le flux depuis lequel charger le document. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Options supplémentaires à utiliser lors du chargement d'un document. Peut être **null**. |
## Remarques


Le document doit être stocké au début du flux. Le flux doit prendre en charge le positionnement aléatoire.

## Exemples



Montre comment ouvrir un document HTML avec des images depuis un flux en utilisant une URI de base.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Passez l'URI du dossier de base lors du chargement.
    // afin que toutes les images avec des URI relatifs dans le document HTML puissent être trouvées.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Vérifiez que la première forme du document contient une image valide.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```


Montre comment charger un document Microsoft Word chiffré.
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// Aspose.Words lève une exception si nous essayons d'ouvrir un document chiffré sans son mot de passe.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// Lors du chargement d'un tel document, le mot de passe est passé au constructeur du document à l'aide d'un objet LoadOptions.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// Il existe deux façons de charger un document chiffré avec un objet LoadOptions.
// 1 -  Chargez le document depuis le système de fichiers local par nom de fichier :
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  Chargez le document depuis un flux :
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## Voir aussi

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&) constructor


Ouvre un document existant à partir d'un fichier. Détecte automatiquement le format du fichier.

```cpp
Aspose::Words::Document::Document(const System::String &fileName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Nom de fichier du document à ouvrir. |

## Exemples



Montre comment ouvrir un document et le convertir en .PDF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToPdf.pdf");
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Ouvre un document existant à partir d'un fichier. Permet de spécifier des options supplémentaires telles qu'un mot de passe de chiffrement.

```cpp
Aspose::Words::Document::Document(const System::String &fileName, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Nom de fichier du document à ouvrir. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Options supplémentaires à utiliser lors du chargement d'un document. Peut être **null**. |

## Exemples



Montre comment créer et charger des documents.
```cpp
// Il existe deux manières de créer un objet Document en utilisant Aspose.Words.
// 1 -  Créez un document vierge :
auto doc = System::MakeObject<Aspose::Words::Document>();

// Les nouveaux objets Document sont, par défaut, fournis avec l'ensemble minimal de nœuds
// nécessaires pour commencer à ajouter du contenu tel que du texte et des formes : une Section, un Corps et un Paragraphe.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  Chargez un document qui existe dans le système de fichiers local :
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Les documents chargés contiendront des éléments que nous pouvons accéder et modifier.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// Certaines opérations qui doivent se produire lors du chargement, comme l'utilisation d'un mot de passe pour déchiffrer un document,
// peuvent être effectuées en passant un objet LoadOptions lors du chargement du document.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


Montre comment charger un document Microsoft Word chiffré.
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// Aspose.Words lève une exception si nous essayons d'ouvrir un document chiffré sans son mot de passe.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// Lors du chargement d'un tel document, le mot de passe est passé au constructeur du document à l'aide d'un objet LoadOptions.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// Il existe deux façons de charger un document chiffré avec un objet LoadOptions.
// 1 -  Chargez le document depuis le système de fichiers local par nom de fichier :
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  Chargez le document depuis un flux :
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## Voir aussi

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream)
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```

## Voir aussi

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
