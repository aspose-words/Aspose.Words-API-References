---
title: License Class
linktitle: License
articleTitle: License
second_title: Aspose.Words per .NET
description: Aspose.Words.License classe. Fornisce metodi per concedere in licenza il componente in C#.
type: docs
weight: 3420
url: /it/net/aspose.words/license/
---
## License class

Fornisce metodi per concedere in licenza il componente.

Per saperne di più, visita il[Licenza e abbonamento](https://docs.aspose.com/words/net/licensing/) articolo di documentazione.

```csharp
public class License
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [License](license/)() | Inizializza una nuova istanza di questa classe. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense)(*Stream*) | Concede in licenza il componente. |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense_1)(*string*) | Concede in licenza il componente. |

## Esempi

Mostra come inizializzare una licenza per Aspose.Words utilizzando un file di licenza nel file system locale.

```csharp
// Imposta la licenza per il nostro prodotto Aspose.Words passando il nome file del file system locale di un file di licenza valido.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Crea una copia del nostro file di licenza nella cartella binaries della nostra applicazione.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Se passiamo il nome di un file senza percorso,
// SetLicense cercherà questo file in diverse posizioni del file system locale.
// Una di queste posizioni sarà la cartella "bin", che contiene una copia del nostro file di licenza.
license.SetLicense("Aspose.Words.NET.lic");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
