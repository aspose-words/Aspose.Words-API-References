---
title: License.SetLicense
second_title: Referencia de API de Aspose.Words para .NET
description: License método. Licencia el componente.
type: docs
weight: 20
url: /es/net/aspose.words/license/setlicense/
---
## SetLicense(string) {#setlicense_1}

Licencia el componente.

```csharp
public void SetLicense(string licenseName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| licenseName | String | Puede ser un nombre de archivo completo o corto o el nombre de un recurso incrustado. Use una cadena vacía para cambiar al modo de evaluación. |

### Observaciones

Intenta encontrar la licencia en las siguientes ubicaciones:

1. Ruta explícita.

2. La carpeta que contiene el ensamblaje del componente Aspose.

3. La carpeta que contiene el ensamblado de llamada del cliente.

4. La carpeta que contiene el ensamblado de entrada (inicio).

5. Un recurso incrustado en el ensamblado de llamadas del cliente.

**Nota:**En .NET Compact Framework, intenta encontrar la licencia solo en estas ubicaciones:

1. Ruta explícita.

2. Un recurso incrustado en el ensamblado de llamada del cliente.

### Ejemplos

Muestra cómo inicializar una licencia para Aspose.Words usando un archivo de licencia en el sistema de archivos local.

```csharp
// Configure la licencia para nuestro producto Aspose.Words pasando el nombre de archivo del sistema de archivos local de un archivo de licencia válido.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Crear una copia de nuestro archivo de licencia en la carpeta de binarios de nuestra aplicación.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Si pasamos el nombre de un archivo sin ruta,
// SetLicense buscará este archivo en varias ubicaciones del sistema de archivos local.
// Una de esas ubicaciones será la carpeta "bin", que contiene una copia de nuestro archivo de licencia.
license.SetLicense("Aspose.Words.NET.lic");
```

### Ver también

* class [License](../)
* espacio de nombres [Aspose.Words](../../license/)
* asamblea [Aspose.Words](../../../)

---

## SetLicense(Stream) {#setlicense}

Licencia el componente.

```csharp
public void SetLicense(Stream stream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | Un flujo que contiene la licencia. |

### Observaciones

Utilice este método para cargar una licencia desde una transmisión.

### Ejemplos

Muestra cómo inicializar una licencia para Aspose.Words desde una secuencia.

```csharp
// Configure la licencia para nuestro producto Aspose.Words pasando una secuencia para un archivo de licencia válido en nuestro sistema de archivos local.
using (Stream myStream = File.OpenRead(Path.Combine(LicenseDir, "Aspose.Words.NET.lic")))
{
    License license = new License();
    license.SetLicense(myStream);
}
```

### Ver también

* class [License](../)
* espacio de nombres [Aspose.Words](../../license/)
* asamblea [Aspose.Words](../../../)


