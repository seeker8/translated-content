---
title: ¿Qué es un nombre de dominio?
slug: Learn/Common_questions/Web_mechanics/What_is_a_domain_name
l10n:
  sourceCommit: d71da812ee94c20658cb1916a123a42254ea545c
---

{{QuicklinksWithSubPages("/es/Learn/Common_questions")}}

<table>
  <tbody>
    <tr>
      <th scope="row">Prerrequisitos:</th>
      <td>
        Primero necesitas saber
        <a href="/es/docs/Learn/How_the_Internet_works"
          >cómo funciona el Internet</a
        >
        y entender
        <a href="/es/Learn/Understanding_URLs">qué son las URLs</a>.
      </td>
    </tr>
    <tr>
      <th scope="row">Objetivo:</th>
      <td>
        Aprende qué son los nombres de dominio, cómo funcionan, y por qué son
        importantes.
      </td>
    </tr>
  </tbody>
</table>

## Resumen

Los nombres de dominio son una parte clave de la infraestructura de internet. Proporcionan una dirección legible para cualquier servidor web disponible en Internet.

Cualquier computadora conectada a Internet puede ser alcanzada a partir de una {{Glossary("IP_Address","dirección IP")}} pública, ya sea una dirección IPv4 (p. ej. `192.0.2.172`) o una dirección IPv6 (p. ej. `2027:0da8:8b73:0000:0000:8a2e:0370:1337`).

Las computadoras pueden manejar estas direcciones fácilmente, pero las personas pasan trabajo para saber de quien es el servidor o que servicio ofrece el sitio web. Las direcciones IP son difíciles de recordar y pueden cambiarse en cualquier momento.

Para resolver estos problemas se usan direcciones que las personas pueden leer, llamadas nombres de dominio.

## Profundizando

### Estructura de los nombres de dominio

Un nombre de dominio tiene una estructura simple formada por varias partes (puede tener solamente una parte, dos, tres,...), separadas por puntos y **se leen de derecha a izquierda**:

![Anatomía del nombre de dominio MDN](structure.png)

Cada una de estas partes provee información específica sobre el nombre de dominio completo.

- {{Glossary("TLD")}} (Top-Level Domain) Dominio de primer nivel.

  - : Los TLDs informan a los usuarios el propósito general del servicio que se esconde tras el nombre de dominio. Los TLDs más genéricos (`.com`, `.org`, `.net`) no requieren que los servicios web cumplan ningún criterio particular, pero algunos TLDs hacen cumplir políticas más estrictas por lo que es más claro su propósito. Por ejemplo:

    - TLDs locales como `.us`, `.fr`, o `.se` pueden requerir el servicio en un determinado idioma o que esté alojado en un país específico - estan hechos para indicar que un recurso está en un idioma o país en particular.
    - Los TLDs que contienen `.gov` son solamente permitidos para ser usados por los departamentos de gobierno.
    - El TLD `.edu` es sólo para uso de instituciones educacionales o académicas.

- Etiqueta (o componente)

  - : Las etiquetas son lo que sigue al TLD. Una etiquta es una secuencia de caracteres que no distingue entre minúsculas o mayúsculas que va desde uno a sesenta y tres caracteres de longitud, contiene solo letras desde la `A` a las `Z`, digitos del `0` al `9` y el caracter `-` (el cual no puede estar ni al inicio ni al final de la etiqueta). `a`, `97`, y `hola-extraño-16-como-estas` son ejemplos de etiquetas validas.

    La etiqueta localizada justo antes de el TLD es llamada _Dominio de Segundo Nivel_ (SLD) por sus siglas en Inglés.

    Un nombre de dominio puede tener muchas etiquetas (o componentes). No es obligatorio o ncesario tener 3 etiquetas para formar un nombre de dominio. Por ejemplo, [informatics.ed.ac.uk](https://informatics.ed.ac.uk/) es un nombre de dominio válido. Por cada dominio bajo tú control (p. ej. [mozilla.org](https://www.mozilla.org/en-US/)), puedes crear "subdominios" con diferente contenido en cada uno, como [developer.mozilla.org](/), [support.mozilla.org](https://support.mozilla.org/), o [bugzilla.mozilla.org](https://bugzilla.mozilla.org/).

### Comprar un nombre de dominio

#### ¿Quién es propietario de un nombre de dominio?

No puedes "comprar un nombre de dominio". Esto es para que en caso de nombres de dominio que no se usan, eventualmente se vuelvan disponibles para que alguien más los use. Si cada nombre de dominio fuera comprado, la web se llenaría rápidamente con nombres de dominio bloqueados que nadie puede usar.

En su lugar, pagas por el derecho de usar un nombre de dominio por uno o más años. Puedes renovar los derechos y la renovación tiene prioridad sobre las aplicaciones de otras personas. Pero nuncá podrás apropiarte de un nombre de dominio.

Las compañías llamadas registradores utilizan los registros de nombres de dominio para realizar un seguimiento de la información técnica y administrativa que lo conecta con su nombre de dominio.

> [!NOTE]
> Para algunos nombres de dominio pudiera no ser un registrador quien esté a cargo de mantener el seguimiento. Por ejemplo, cada nombre de dominio bajo `.fire` es manejado por Amazon.

#### Encontrar un nombre de dominio disponible

Para encontrar si un nombre de dominio dado está disponible,

- Ve a un sitio web de registro de nombres de dominio. La mayoría de ellos, tienen un servicio "whois" que te dice si un nombre de dominio está disponible.
- Alternativamente, si usas un sistema con un shell incorporado, escribe el comando `whois`, como se muestra aquí para `mozilla.org`:

```
$ whois mozilla.org
Domain Name:MOZILLA.ORG
Domain ID: D1409563-LROR
Creation Date: 1998-01-24T05:00:00Z
Updated Date: 2013-12-08T01:16:57Z
Registry Expiry Date: 2015-01-23T05:00:00Z
Sponsoring Registrar:MarkMonitor Inc. (R37-LROR)
Sponsoring Registrar IANA ID: 292
WHOIS Server:
Referral URL:
Domain Status: clientDeleteProhibited
Domain Status: clientTransferProhibited
Domain Status: clientUpdateProhibited
Registrant ID:mmr-33684
Registrant Name:DNS Admin
Registrant Organization:Mozilla Foundation
Registrant Street: 650 Castro St Ste 300
Registrant City:Mountain View
Registrant State/Province:CA
Registrant Postal Code:94041
Registrant Country:US
Registrant Phone:+1.6509030800
```

Como puedes ver, no puedo registrar `mozilla.org` porque la fundación de Mozilla ya ha sido registrada.

Por otra parte, veamos si se puede registrar `afunkydomainname.org`:

```
$ whois afunkydomainname.org
NOT FOUND
```

Como puedes ver, el dominio no existe en la base de datos de `whois` (en el momento que se escribió), por lo que pudiéramos pedir registrarlo. ¡Bueno para saber!

#### Obtener un nombre de dominio

El proceso es bastante sencillo:

1. Ir a un sitio de registro.
2. Generalmente hay un letrero que llama la atención que dice "Get a domain name". Hacer click en él.
3. Rellenar el formulario con todos los detalles requeridos. Asegúrese de no haber escrito incorrectamente el nombre de dominio deseado. ¡Una vez que esté pagado, es muy tarde!.
4. El registrador te permitirá conocer cuando un nombre de dominio esté correctamente registrado. Dentro de unas pocas horas, todos los servidores DNS habrán recibido su información de DNS.

> [!NOTE]
> En este proceso se le pide su dirección real. Asegúrese de escribirla correctamente, ya que en algunos países los registradores pueden verse obligados a cerrar el dominio si no pueden proporcionar una dirección válida.

#### Actualización de DNS

Las bases de datos DNS son almacenadas en cada servidor DNS del mundo, y todos ellos hacen referencia a unos pocos denominados "servidores de nombre autoritario" o "servidores DNS de primer nivel", estos son como los servidores jefe que administran el sistema. 

Cuando su registrador crea o actualiza alguna información para un dominio dado, la información tiene que ser actualizada en cada base de datos DNS. Cada servidor DNS que conoce sobre un dominio dado almacena la información por algún tiempo antes de que sea automáticamente invalidada y luego actualizada ( el servidor DNS consulta un servidor autoritario nuevamente). De esta manera, a los servidores DNS que conocen este nombre de dominio les toma algún tiempo poner la información al día.

### ¿Cómo funciona una petición DNS?

Como ya hemos visto, cuando quieres visualizar una página web en tú navegador, es más simple escribir un nombre de dominio que una dirección IP. Echemos un vistazo al proceso:

1. Escribe `mozilla.org` en la barra de direcciones de tú navegador.
2. Tú navegador le pregunta a su computadora si reconoce la dirección IP identificada por este nombre de dominio (usando una caché DNS local) Si lo hace, el nombre es traducido a la IP y el navegador gestiona el contenido con el servidor web. Fin de la historia.
3. Si la computadora no sabe qué IP está detrás del nombre `mozilla.org`, hay que pedírselo a un servidor DNS, cuyo trabajo es precisamente decirle a la computadora cuál es la dirección IP de cada nombre de dominio registrado.
4. Ahora que la computadora conoce la dirección IP requerida, tú navegador puede gestionar contenidos con el servidor web.

![Explicación de los pasos necesarios para obtener el resultado de una solicitud DNS](2014-10-dns-request2.png)

## Próximos pasos

Bien, hemos hablado mucho sobre procesos y arquitectura. Es hora de seguir adelante.

- Si quieres ponerte manos a la obra, es buen momento para comenzar a profundizar en el diseño y explorar [la estructura de una página web](/es/docs/Learn/Common_questions/dise%C3%B1os_web_comunes).
- Vale la pena señalar que algunos aspectos de construcción de un sitio web cuestan dinero. Por favor, remítase a [cuánto cuesta construir un sitio web](/es/docs/Learn/How_much_does_it_cost).
- O lea más sobre [Nombre de Dominio](https://es.wikipedia.org/wiki/Dominio) en la Wikipedia.
- También puedes encontrar [aquí](https://howdns.works/) una explicación colorida y divertida de cómo los DNS trabajan.
