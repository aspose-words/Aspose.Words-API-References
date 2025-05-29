---
title: ReportingEngine.SetRestrictedTypes
linktitle: SetRestrictedTypes
articleTitle: SetRestrictedTypes
second_title: Aspose.Words para .NET
description: Descubra cómo el método SetRestrictedTypes en ReportingEngine mejora la seguridad al limitar el acceso de los miembros en la sintaxis de plantilla para generar informes de datos optimizados.
type: docs
weight: 80
url: /es/net/aspose.words.reporting/reportingengine/setrestrictedtypes/
---
## ReportingEngine.SetRestrictedTypes method

Especifica los tipos, qué miembros, así como los miembros de los tipos derivados, deben ser inaccesibles para el motor a través de la sintaxis de plantilla.

```csharp
public static void SetRestrictedTypes(params Type[] types)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| types | Type[] | Tipos a restringir. |

## Observaciones

Los tipos restringidos deben configurarse antes de la primera creación de un informe. Después`Informe de construcción` Se invoca, los tipos restringidos no se pueden modificar y se genera una excepción al intentar hacerlo. El mejor lugar para configurar los tipos restringidos es al iniciar la aplicación.

Tenga en cuenta que una gran cantidad de tipos restringidos puede afectar el rendimiento, por lo que es mejor restringir solo aquellos tipos cuyo acceso a miembros es realmente sensible.

LanzamientosArgumentException en los siguientes casos:

-*types* es nulo.

- Uno de*types* Los artículos son`nulo`.

- Uno de*types* items representa un tipo invisible, es decir, un tipo no público o un tipo público anidado que tiene un tipo externo no público.

- Uno de*types* items representa un tipo de matriz.

-*types* Contiene entradas duplicadas.

## Ejemplos

Muestra cómo denegar el acceso a miembros de tipos considerados inseguros.

```csharp
Document doc =
    DocumentHelper.CreateSimpleDocument(
        "<<var [typeVar = \"\".GetType().BaseType]>><<[typeVar]>>");

// Tenga en cuenta que no es posible establecer tipos restringidos durante o después de crear un informe.
ReportingEngine.SetRestrictedTypes(typeof(System.Type));
// Establecemos la opción "AllowMissingMembers" para evitar excepciones durante la creación de un informe.
ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.AllowMissingMembers };
engine.BuildReport(doc, new object());

// Obtenemos una cadena vacía porque no podemos acceder al método GetType().
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### Ver también

* class [ReportingEngine](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)
