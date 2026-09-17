---
title: "Méthode Aspose::Words::FileFormatInfo::get_Encoding"
linktitle: "get_Encoding"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::FileFormatInfo::get_Encoding. Obtient le codage détecté si applicable au format du document actuel. Pour le moment, il ne détecte le codage que pour les documents HTML en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/fileformatinfo/get_encoding/
---
## FileFormatInfo::get_Encoding method


Obtient l'encodage détecté si applicable au format du document actuel. Pour le moment, il ne détecte l'encodage que pour les documents HTML.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::FileFormatInfo::get_Encoding() const
```


## Exemples



Montre comment détecter l’encodage dans un fichier HTML.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.html");

ASSERT_EQ(Aspose::Words::LoadFormat::Html, info->get_LoadFormat());

// La propriété Encoding n'est utilisée que lorsque nous créons un objet FileFormatInfo pour un document html.
ASSERT_EQ(u"Western European (Windows)", info->get_Encoding()->get_EncodingName());
ASSERT_EQ(1252, info->get_Encoding()->get_CodePage());
```

## Voir aussi

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
