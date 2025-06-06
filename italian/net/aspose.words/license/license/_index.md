---
title: License
linktitle: License
articleTitle: License
second_title: Aspose.Words per .NET
description: Crea e gestisci le licenze senza sforzo con la nostra classe di costruttori. Semplifica il tuo processo di licenza e migliora l'efficienza oggi stesso!
type: docs
weight: 10
url: /it/net/aspose.words/license/license/
---
## License constructor

Inizializza una nuova istanza di questa classe.

```csharp
public License()
```

## Esempi

Mostra come inizializzare una licenza per Aspose.Words utilizzando un file di licenza nel file system locale.

```csharp
// Imposta la licenza per il nostro prodotto Aspose.Words passando il nome file del file system locale di un file di licenza valido.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Creiamo una copia del nostro file di licenza nella cartella binari della nostra applicazione.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Se passiamo il nome di un file senza un percorso,
// SetLicense cercherà questo file in diverse posizioni del file system locale.
// Una di queste posizioni sarà la cartella "bin", che contiene una copia del nostro file di licenza.
license.SetLicense("Aspose.Words.NET.lic");
```

### Guarda anche

* class [License](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
