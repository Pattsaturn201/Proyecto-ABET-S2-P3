#include <stdio.h>

// Definición de la estructura de una máquina
struct Maquina {
    char nombre[20];
    float materia_prima_utilizada;
    float materia_prima_desperdiciada;
};

// Función para calcular el porcentaje de desperdicio
float calcularPorcentajeDesperdicio(float utilizada, float desperdiciada) {
    if (utilizada > 0) {
        return (desperdiciada / utilizada) * 100.0;
    } else {
        return 0.0;
    }
}

int main() {
    // Declaración de las tres máquinas
    struct Maquina maquinas[3] = {
        {"Maquina 1", 1000.0, 50.0}, // Ejemplo de valores utilizados para la máquina 1
        {"Maquina 2", 800.0, 30.0},  // Ejemplo de valores utilizados para la máquina 2
        {"Maquina 3", 1200.0, 60.0}  // Ejemplo de valores utilizados para la máquina 3
    };

    // Apertura del archivo de texto para escritura
    FILE *archivo = fopen("resultados.txt", "w");
    if (archivo == NULL) {
        printf("Error al abrir el archivo.");
        return 1;
    }

    // Calcula el porcentaje de desperdicio para cada máquina y escribe los resultados en el archivo
    for (int i = 0; i < 3; i++) {
        float porcentaje_desperdicio = calcularPorcentajeDesperdicio(maquinas[i].materia_prima_utilizada, maquinas[i].materia_prima_desperdiciada);
        fprintf(archivo, "Maquina: %s\n", maquinas[i].nombre);
        fprintf(archivo, "Porcentaje de materia prima desperdiciada: %.2f%%\n\n", porcentaje_desperdicio);
    }

    // Cierre del archivo
    fclose(archivo);

    printf("Los resultados se han guardado en el archivo 'resultados.txt'.\n");

    return 0;
}
