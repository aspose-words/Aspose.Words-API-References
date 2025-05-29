---
title: License.SetLicense
linktitle: SetLicense
articleTitle: SetLicense
second_title: Aspose.Words per .NET
description: Ottieni la licenza dei tuoi componenti senza sforzo con il nostro metodo SetLicense. Sblocca tutte le funzionalità e aumenta il potenziale del tuo progetto oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words/license/setlicense/
---
## SetLicense(*string*) {#setlicense_1}

Concede la licenza del componente.

```csharp
public void SetLicense(string licenseName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| licenseName | String | Può essere un nome di file completo o breve oppure il nome di una risorsa incorporata. Utilizzare una stringa vuota per passare alla modalità di valutazione. |

## Osservazioni

Prova a trovare la licenza nelle seguenti posizioni:

1. Percorso esplicito.

2. La cartella che contiene l'assemblaggio del componente Aspose.

3. La cartella che contiene l'assembly chiamante del client.

4. La cartella che contiene l'assembly di ingresso (avvio).

5. Una risorsa incorporata nell'assembly chiamante del client.

**Nota:**In .NET Compact Framework, prova a trovare la licenza solo in queste posizioni:

1. Percorso esplicito.

2. Una risorsa incorporata nell'assembly chiamante del client.

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

---

## SetLicense(*Stream*) {#setlicense}

Concede la licenza del componente.

```csharp
public void SetLicense(Stream stream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Un flusso che contiene la licenza. |

## Osservazioni

Utilizzare questo metodo per caricare una licenza da un flusso.

## Esempi

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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
