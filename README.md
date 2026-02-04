# qa-practice-project
Proyecto de Práctica QA: Análisis de Spotify

Objetivo: Aplicar metodologías de Testing QA en un entorno real (Spotify Web) para practicar el ciclo completo de control de calidad, desde el análisis hasta el reporte de bugs

 [Descripción del Proyecto]
| Aplicación bajo prueba | Spotify Web (open.spotify.com) |
| Rol | QA Trainee / Tester Autogestionado |
| Alcance de pruebas | Módulos de Búsqueda, Reproducción y Gestión de Playlists. |
| Tipo de pruebas | Funcionales, de Usabilidad y Flujos de Usuario |
| Herramientas utilizadas: | Navegador Chrome, Google Sheets, GitHub |


[Proceso a Seguir (Metodología QA)]
1.  Análisis de Requisitos: Observar comportamiento esperado de la aplicación basado en la experiencia del usuario y documentación pública.
2.  Planificación de Pruebas: Identificación de funcionalidades críticas y diseño de una estrategia de prueba.
3.  Diseño de Casos de Prueba: Creación de casos detallados y específicos para cada flujo
4.  Ejecución: Prueba manual de los casos en el entorno de producción (En este caso su versión Web)
5.  Reporte y Documentación: Registro estructurado de bugs, priorizando por impacto en el usuario.


[Ejemplos de Casos de Prueba]
(En la carpeta ["TestCases"] se puede ver la versión extendida de los Casos Diseñados. 
Este es un extracto de dichos casos:

| ID Caso |    Módulo    | Caso de Prueba | Datos de Entrada | Resultado Esperado | Estado |
|---------|--------------|----------------|------------------|--------------------|--------|
| CP-01   | Búsqueda     | Buscar un artista existente | "Dua Lipa" | Se muestra el perfil del artista con sus álbumes y canciones top. | ✅ Pasó |
| CP-02   | Búsqueda     | Buscar con caracteres especiales | "@#$%" | Muestra mensaje "No encontramos" o sugerencias. | ✅ Pasó |
| CP-03   | Reproducción | Reproducir una canción desde la vista de álbum | Click en "Play" en un álbum | La canción se reproduce, la barra de progreso avanza y el ícono cambia a "Pause". | ✅ Pasó |
| CP-04   | Playlist     | Crear una playlist vacía | Click en "Crear playlist", nombre "Pruebas QA" | La playlist aparece en la barra lateral con 0 canciones. | ✅ Pasó |
| CP-05   | Playlist     | Agregar una canción a una playlist desde "Buscar" | Drag & Drop de una canción a la playlist | La playlist muestra +1 canción y la canción se agrega al final. | ✅ Pasó |




[Ejemplo de Reporte de Bug Documentado]

Título: El botón "Me gusta" no da feedback visual claro al ser activado en la barra de reproducción inferior.
- ID: "BUG-SPOTIFY-001"
- Severidad: Baja ("Posible incomodidad a Usuarios")
- Prioridad: Baja ("Debería ser corregido, sin embargo no es de alta prioridad")
- Módulo / Página: Barra de reproducción inferior (Reproductor universal).
- Navegador / SO: Navegador Brave / Windows 11.
- URL: https://open.spotify.com/

*Pasos para Reproducir:
1.  Iniciar sesión en Spotify Web.
2.  Buscar y reproducir cualquier canción.
3.  En la barra de reproducción inferior (fija al pie), hacer clic en el botón "Me gusta" (corazón) para activarlo.
4.  Observar el botón.

*Resultado Esperado:
- El botón debe cambiar a un estado en que se vea lleno con el color verde del Like, o mostrar un tooltip que confirme que la canción se ha agregado a "Tus Me gusta".
- Debe persistir el estado si se navega a otra página.

*Resultado Obtenido:
- El botón cambia brevemente a su forma "Llena" y luego vuelve a su estado vacío, dando la impresión de que no se ha guardado la acción.
- La canción **SÍ** se agrega a la biblioteca "Tus Me gusta", pero la UI no lo refleja de forma consistente.




[Conclusión y Finalización]

La finalidad de este proyecto es:
- Practicar la creación de artefactos de QA
- Replicar y analizar los pasos detallados y reproducibles en un reporte.
- Evaluar la experiencia del usuario más allá de la funcionalidad básica.
- Priorizar y balancear los "Bugs" o posibles fallas basado en su impacto (Severidad vs. Prioridad)






















