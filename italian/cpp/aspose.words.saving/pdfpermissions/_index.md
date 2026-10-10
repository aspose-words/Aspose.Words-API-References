---
title: "Aspose::Words::Saving::PdfPermissions enum"
linktitle: "PdfPermissions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::PdfPermissions enum. Specifica le operazioni consentite a un utente su un documento PDF crittografato in C++."
type: docs
weight: 80000
url: /it/cpp/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enum


Specifica le operazioni consentite a un utente su un documento PDF crittografato.

```cpp
enum class PdfPermissions
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| DisallowAll | 0 | Disabilita tutte le operazioni sul documento PDF. Questo è il valore predefinito. |
| AllowAll | 65535 | Consente tutte le operazioni sul documento PDF. |
| ContentCopy | n/a | Copia o estrae in altro modo testo e grafica dal documento mediante operazioni diverse da quelle controllate da [ContentCopyForAccessibility](./). |
| ContentCopyForAccessibility | n/a | Estrai testo e grafica (a supporto dell'accessibilità per utenti con disabilità o per altri scopi). |
| ModifyContents | n/a | Modifica il contenuto del documento mediante operazioni diverse da quelle controllate da [ModifyAnnotations](./), [FillIn](./) e [DocumentAssembly](./). |
| ModifyAnnotations | n/a | Aggiungi o modifica annotazioni di testo, compila campi di modulo interattivi e, se [ModifyContents](./) è anche impostato, crea o modifica campi di modulo interattivi (inclusi i campi firma). |
| FillIn | n/a | Compila i campi di modulo interattivi esistenti (inclusi i campi firma), anche se [ModifyContents](./) è disattivato. |
| DocumentAssembly | n/a | Assembla il documento (inserisci, ruota o elimina pagine e crea voci di indice del documento o immagini in miniatura), anche se [ModifyContents](./) è disattivato. |
| Printing | n/a | Stampa il documento (potenzialmente non al livello di qualità più alto, a seconda se [HighResolutionPrinting](./) è anche impostato). |
| HighResolutionPrinting | n/a | Stampa il documento in una rappresentazione da cui può essere generata una copia digitale fedele del contenuto PDF, basata su un algoritmo dipendente dall'implementazione. Quando questa opzione è disattivata (e [Printing](./) è impostato), la stampa deve essere limitata a una rappresentazione di basso livello dell'aspetto, possibilmente di qualità ridotta. |

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
