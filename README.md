# programa-python
# Fase  5
# Nombre del estudiante: KAREN YULIETH PUENTES VARGAS
# Grupo: 256
# Programa: INGIENERIA EN SISTEMAS
# Código Fuente: DE MI AUTORIA 
# Descripción: Una matriz registra las horas trabajadas por un equipo 
# SOLICITADO POR ALMACEN DE COMPRAS 
equipo = [
    ["Ana", 8, 9, 8, 8, 9],
    ["Luis", 7, 8, 7, 8, 7],
    ["Carlos", 9, 10, 9, 10, 9],
    ["Maria", 8, 8, 8, 8, 8]
]

def calcular_total_horas(horas):
    total = 0
    for h in horas:
        total += h
    return total

def clasificar_jornada(total_horas):
    if total_horas > 40:
        return "Sobretiempo"
    else:
        return "Horario Estándar"

def procesar_recurso(recurso):
    nombre = recurso[0]
    horas = recurso[1:]
    total = calcular_total_horas(horas)
    clasificacion = clasificar_jornada(total)
    return nombre, total, clasificacion

print("REPORTE DE HORAS SEMANALES")

for persona in equipo:
    nombre, total, estado = procesar_recurso(persona)
    print("Recurso:", nombre)
    print("Total de horas:", total)
    print("Clasificación:", estado)
