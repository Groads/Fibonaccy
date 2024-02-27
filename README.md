class GeneradorFibonacci:
    def __init__(self, cantidad):
        self.cantidad = cantidad
        self.sec_fibonacci = [0, 1]

    def generar_secuencia(self):
        while len(self.sec_fibonacci) < self.cantidad:
            self.sec_fibonacci.append(self.sec_fibonacci[-1] + self.sec_fibonacci[-2])

    def obtener_secuencia(self):
        return self.sec_fibonacci

cantidad_terminos = int(input("Ingrese la cantidad de términos en la serie de Fibonacci: "))

generador_fibonacci = GeneradorFibonacci(cantidad_terminos)

generador_fibonacci.generar_secuencia()

resultado = generador_fibonacci.obtener_secuencia()

print(f"Serie de Fibonacci con {cantidad_terminos} términos: {resultado}")
