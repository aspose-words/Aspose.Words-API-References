---
title: "Metodo Aspose::Words::Saving::PdfEncryptionDetails::get_UserPassword"
linktitle: "get_UserPassword"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::PdfEncryptionDetails::get_UserPassword. Specifica la password dell'utente necessaria per aprire il documento PDF crittografato in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.saving/pdfencryptiondetails/get_userpassword/
---
## PdfEncryptionDetails::get_UserPassword method


Specifica la password utente necessaria per aprire il documento PDF crittografato.

```cpp
System::String Aspose::Words::Saving::PdfEncryptionDetails::get_UserPassword() const
```

## Note


La password dell'utente sarà necessaria per aprire un documento PDF crittografato per la visualizzazione. Le autorizzazioni specificate in [Permissions](../get_permissions/) saranno applicate dal software di lettura.

La password dell'utente può essere **null** o una stringa vuota; in questo caso non sarà richiesta alcuna password all'utente durante l'apertura del documento PDF. La password dell'utente non può essere uguale alla password del proprietario.
## Vedi anche

* Class [PdfEncryptionDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
