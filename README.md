from graphviz import Digraph

def crear_organigrama():
    dot = Digraph()

    # Agregar nodos
    dot.node('JefeLogistica', 'Jefe de Logística')
    dot.node('ServicioCliente', 'Servicio al Cliente')
    dot.node('ProduccionSupervision', 'Producción y Supervisión')
    dot.node('Almacenista', 'Almacenista')
    dot.node('Operativa', 'Operativa')
    dot.node('Transporte', 'Transporte')
    dot.node('TecnicoAsistencia', 'Técnico en Asistencia')
    dot.node('Conductores', 'Conductores')

    # Agregar relaciones
    dot.edge('JefeLogistica', 'ServicioCliente')
    dot.edge('JefeLogistica', 'ProduccionSupervision')
    dot.edge('JefeLogistica', 'Almacenista')
    dot.edge('JefeLogistica', 'Operativa')
    dot.edge('JefeLogistica', 'Transporte')
    dot.edge('JefeLogistica', 'TecnicoAsistencia')
    dot.edge('JefeLogistica', 'Conductores')

    # Generar archivo
    dot.render('organigrama_logistica', format='png')

if __name__ == "__main__":
    crear_organigrama()
