---
title: "Méthode Aspose::Words::Font::get_LocaleId"
linktitle: "get_LocaleId"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::get_LocaleId. Obtient ou définit l'identifiant de paramètre régional (langue) des caractères formatés en C++."
type: docs
weight: 22000
url: /fr/cpp/aspose.words/font/get_localeid/
---
## Font::get_LocaleId method


Obtient ou définit l'identifiant de paramètre régional (langue) des caractères formatés.

```cpp
int32_t Aspose::Words::Font::get_LocaleId()
```


## Exemples



Montre comment définir le paramètre régional du texte que nous ajoutons avec un constructeur de document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Si nous définissons le paramètre régional de la police sur l'anglais et insérons du texte russe,
// le correcteur orthographique anglais ne reconnaîtra pas le texte et le signalera comme une faute d'orthographe.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());
builder->Writeln(u"Привет!");

// Définissez un paramètre régional correspondant pour le texte que nous allons ajouter afin d'appliquer le correcteur orthographique approprié.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"ru-RU", false)->get_LCID());
builder->Writeln(u"Привет!");

doc->Save(get_ArtifactsDir() + u"Font.LocaleId.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
