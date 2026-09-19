---
title: "Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter metodo"
linktitle: "get_IgnoreHeaderFooter"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter metodo. Ottiene o imposta un valore booleano che specifica che la formattazione di origine del contenuto di intestazioni/piè di pagina viene ignorata se viene utilizzata la modalità KeepSourceFormatting. Il valore predefinito è true in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words/importformatoptions/get_ignoreheaderfooter/
---
## ImportFormatOptions::get_IgnoreHeaderFooter method


Ottiene o imposta un valore booleano che specifica che la formattazione di origine del contenuto di intestazioni/piè di pagina viene ignorata se viene utilizzata la modalità [KeepSourceFormatting](../../importformatmode/). Il valore predefinito è **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter() const
```


## Esempi



Mostra come specificare l'ignorare o meno la formattazione di origine del contenuto di intestazioni/piè di pagina.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Se 'IgnoreHeaderFooter' è false, allora la formattazione originale per il contenuto di intestazione/piè di pagina
// da "Header and footer types.docx" verrà utilizzato.
// Se 'IgnoreHeaderFooter' è true allora la formattazione per il contenuto header/footer.
// da "Document.docx" verrà utilizzato.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_IgnoreHeaderFooter(false);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importFormatOptions);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

## Vedi anche

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
