# comandos del editor de etiquetas mp3 llamado id3v2

📋 Opciones generales

-h, --help
Muestra la ayuda y sale  .

 --version
Muestra la versión del programa  .


Listar información

-l, --list [ARCHIVOS...]
Lista las etiquetas ID3v2 de los archivos  .


-f, --list-frames
Muestra todos los posibles frames de ID3v2  .

-lg, --list-genres
Muestra la lista de géneros en ID3v1  .


Eliminar etiquetas

 --eliminar-v2 [ARCHIVOS...]
Elimina únicamente las etiquetas ID3v2  .

 --eliminar-v1 [ARCHIVOS...]
Elimina únicamente las etiquetas ID3v1  .

--eliminar-all [ARCHIVOS...]
Elimina ambas etiquetas, v1 y v2  .


Conversión

-C, --convert [ARCHIVOS...]
Convierte etiquetas v1 a v2  .


Establecer campos básicos

-a, --artista ARTISTA
Establece el artista  .

-A, --album ÁLBUM
Establece el título del álbum  .

-t, --titulo TEMA
Establece el título de la canción  .

-c, --comentario DESCRIPCIÓN:COMENTARIO[:IDIOMA]
Establece un comentario (puede incluir idioma opcional)  .

-g, --genre NÚM
Establece el género (número según lista)  .

-y, --año AÑO
Establece el año  .

-T, --track NUM[/TOTAL]
Establece el número de pista (y opcionalmente total de pista)  .


Opciones avanzadas

--FRAMEID VALOR
Permite establecer cualquier frame específico de ID3v2 (por ejemplo: --TIT3 "Subtítulo" archivo.mp3)  .

-1, --id3v1-only
Solo escribe etiquetas ID3v1  .

-2, --id3v2-only
Solo escribe etiquetas ID3v2  .

-r, --remove-frame FRAMEID
Elimina un frame v2 específico  .

-p, --picture ARCHIVO y --APIC TIPO
Adjunta una imagen (cover art) con tipo específico  .

-v NUM
Define la versión de ID3v2 a utilizar (usualmente 3 o 4)  .

-m
Conserva la fecha/hora del archivo (no modifica timestamp)  .

-q
Modo silencioso, sin salidas por pantalla  .



---

🛠 Ejemplos útiles

# Ver etiquetas v2 de un archivo:
id3v2 --list pista.mp3

# Establecer artista, canción y álbum:
id3v2 -a "Artista" -t "Título" -A "Álbum" pista.mp3

# Eliminar todas las etiquetas ID3:
id3v2 -D pista.mp3

# Convertir v1 a v2 en varios archivos:
id3v2 -C *.mp3

# Adjuntar portada (APIC):
id3v2 -p portada.jpg --APIC "Front cover" pista.mp3

# Establecer cualquier frame, ejemplo: subtítulo:
id3v2 --TIT3 "Subtítulo" pista.mp3


