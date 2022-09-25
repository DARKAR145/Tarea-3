#**Esquema modelo relacional**

Videojuego(ID, Nombre, Desarrollador, Publicador)

Torneo(Id, Direccion, Estado, Inicio_de_torneo, Fin_de_torneo, ID del videojuego)

Partido(Id, Id Equipo Izquierdo, ID Equipo Derecho, Fecha y Hora, Fallas, Resultado, Duracion, Id torneo)

Equipo(ID, # Integrantes, Logo, Nombre, Color)

Jugador(ID, Edad, Nacionalidad, Id equipo)

Jugador/Partido(ID Jugador, ID Partido, Total Kills, Total Muertes, KD, KAD)

```mermaid
erDiagram 
Videojuego ||--}o Torneo : ""
Torneo ||--}o Partido : ""
  Partido ||--}o Equipo : "Local"
  Partido ||--}o Equipo : "Visitante"
  Jugador o{--}o Equipo : ""
  Jugador-Partido ||--}o Jugador : ""
  Jugador-Partido ||--}o Partido : ""
  Torneo {
    entero id
    texto id_videojuego
    fecha inicio_de_torneo
    fecha fin_de_torneo
    texto direccion
    texto estado
    texto pais
  }
  Videojuego {
    entero ID
    texto Nombre
    texto Desarrollador
    texto Publicador
  }
  Equipo {
     entero ID
     numerico Numero de integrantes
     imagen Logo
     texto Nombre
     texto Color
  }
  Partido {
    entero ID
    texto Fecha_y_Hora
    entero Id Equipo derecho
    entero ID Equipo Izquierdo
    texto Fallas
    texto Resultado
    texto Duracion
  }
  Jugador {
    entero Id
    numerico edad
    texto Nacionalidad
    entero Id_equipo
  }

  Jugador-Partido {
    entero Id_Jugador
    entero Id_partido
    numerico Total_Kills
    numerico Total_muertes
    numerico KD
    numerico KAD
  }