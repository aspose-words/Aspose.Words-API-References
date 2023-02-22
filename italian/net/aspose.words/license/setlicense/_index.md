---
title: License.SetLicense
second_title: Aspose.Words per .NET API Reference
description: License metodo. concede in licenza il componente.
type: docs
weight: 20
url: /it/net/aspose.words/license/setlicense/
---
## SetLicense(string) {#setlicense_1}

concede in licenza il componente.

```csharp
public void SetLicense(string licenseName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| licenseName | String | Può essere un nome file completo o breve o il nome di una risorsa incorporata. Utilizzare una stringa vuota per passare alla modalità di valutazione. |

### Osservazioni

Cerca di trovare la licenza nelle seguenti posizioni:

1. Percorso esplicito.

2. La cartella che contiene l'assieme del componente Aspose.

3. La cartella che contiene l'assembly chiamante del client.

4. La cartella che contiene l'assembly voce (avvio).

5. Una risorsa incorporata nell'assembly chiamante del client.

**Nota:**In .NET Compact Framework, prova a trovare la licenza solo in queste posizioni:

1. Percorso esplicito.

2. Una risorsa incorporata nell'assembly chiamante del client.

### Esempi

Mostra come inizializzare una licenza per Aspose.Words utilizzando un file di licenza nel file system locale.

```csharp
// Imposta la licenza per il nostro prodotto Aspose.Words passando il nome file del file system locale di un file di licenza valido.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Crea una copia del nostro file di licenza nella cartella binari della nostra applicazione.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Se passiamo il nome di un file senza un percorso,
// SetLicense cercherà questo file in diverse posizioni del file system locale.
// Una di queste posizioni sarà la cartella "bin", che contiene una copia del nostro file di licenza.
license.SetLicense("Aspose.Words.NET.lic");
```

### Guarda anche

* class [License](../)
* spazio dei nomi [Aspose.Words](../../license/)
* assemblea [Aspose.Words](../../../)

---

## SetLicense(Stream) {#setlicense}

concede in licenza il componente.

```csharp
public void SetLicense(Stream stream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Un flusso che contiene la licenza. |

### Osservazioni

Utilizzare questo metodo per caricare una licenza da uno stream.

### Esempi

Mostra come inizializzare una licenza per Aspose.Words da un flusso.

```csharp
// Imposta la licenza per il nostro prodotto Aspose.Words passando un flusso per un file di licenza valido nel nostro file system locale.
using (Stream myStream = File.OpenRead(Path.Combine(LicenseDir, "Aspose.Words.NET.lic")))
{
    License license = new License();
    license.SetLicense(myStream);
}
```

### Guarda anche

* class [License](../)
* spazio dei nomi [Aspose.Words](../../license/)
* assemblea [Aspose.Words](../../../)


