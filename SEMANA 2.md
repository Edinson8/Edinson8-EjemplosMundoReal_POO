using System;

namespace FigurasGeometricas
{
    // Clase Círculo que encapsula el tipo de dato primitivo para el radio
    public class Circulo
    {
        // Atributo para almacenar el radio del círculo
        private double radio;

        // Constructor para inicializar el radio del círculo
        public Circulo(double radio)
        {
            this.radio = radio;
        }

        // Método para calcular el área de un círculo
        // El área de un círculo se calcula con la fórmula A = π * r²
        public double CalcularArea()
        {
            return Math.PI * radio * radio;  // Devuelve el área calculada
        }

        // Método para calcular el perímetro (circunferencia) de un círculo
        // El perímetro se calcula con la fórmula P = 2 * π * r
        public double CalcularPerimetro()
        {
            return 2 * Math.PI * radio;  // Devuelve el perímetro calculado
        }
    }

    // Clase Rectángulo que encapsula los tipos de datos primitivos para el largo y ancho
    public class Rectangulo
    {
        // Atributos para almacenar el largo y el ancho del rectángulo
        private double largo;
        private double ancho;

        // Constructor para inicializar el largo y el ancho del rectángulo
        public Rectangulo(double largo, double ancho)
        {
            this.largo = largo;
            this.ancho = ancho;
        }

        // Método para calcular el área de un rectángulo
        // El área de un rectángulo se calcula con la fórmula A = largo * ancho
        public double CalcularArea()
        {
            return largo * ancho;  // Devuelve el área calculada
        }

        // Método para calcular el perímetro de un rectángulo
        // El perímetro se calcula con la fórmula P = 2 * (largo + ancho)
        public double CalcularPerimetro()
        {
            return 2 * (largo + ancho);  // Devuelve el perímetro calculado
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            // Creación de un objeto de la clase Circulo con un radio de 5
            Circulo miCirculo = new Circulo(5);
            // Imprimir el área y perímetro del círculo
            Console.WriteLine("Área del Círculo: " + miCirculo.CalcularArea());
            Console.WriteLine("Perímetro del Círculo: " + miCirculo.CalcularPerimetro());

            // Creación de un objeto de la clase Rectangulo con un largo de 10 y un ancho de 5
            Rectangulo miRectangulo = new Rectangulo(10, 5);
            // Imprimir el área y perímetro del rectángulo
            Console.WriteLine("Área del Rectángulo: " + miRectangulo.CalcularArea());
            Console.WriteLine("Perímetro del Rectángulo: " + miRectangulo.CalcularPerimetro());

            // Mantener la ventana abierta para ver los resultados
            Console.ReadLine();
        }
    }
}
