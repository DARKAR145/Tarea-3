#**Esquema modelo relacional**

Videojuego(ID, Nombre, Desarrollador, Publicador)

Torneo(Id, Direccion, Estado, Inicio_de_torneo, Fin_de_torneo, ID del videojuego)

Partido(Id, Id Equipo Izquierdo, ID Equipo Derecho, Fecha y Hora, Fallas, Resultado, Duracion, Id torneo)

Equipo(ID, # Integrantes, Logo, Nombre, Color)

Jugador(ID, Edad, Nacionalidad, Id equipo)

Jugador/Partido(ID Jugador, ID Partido, Total Kills, Total Muertes, KD, KAD)