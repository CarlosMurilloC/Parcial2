/**
 * La clase Empleado representa a un empleado en una empresa.
 */
public class Empleado {
    private String nombre; // Nombre del empleado
    private String cargo; // Cargo del empleado
    private double salario; // Salario del empleado

    /**
     * Constructor para crear un nuevo objeto Empleado.
     *
     * @param nombre  Nombre del empleado.
     * @param cargo   Cargo del empleado.
     * @param salario Salario del empleado.
     */
    public Empleado(String nombre, String cargo, double salario) {
        this.nombre = nombre;
        this.cargo = cargo;
        this.salario = salario;
    }

    /**
     * Obtiene el nombre del empleado.
     *
     * @return Nombre del empleado.
     */
    public String getNombre() {
        return nombre;
    }

    /**
     * Establece el nombre del empleado.
     *
     * @param nombre Nuevo nombre del empleado.
     */
    public void setNombre(String nombre) {
        this.nombre = nombre;
    }

    /**
     * Obtiene el cargo del empleado.
     *
     * @return Cargo del empleado.
     */
    public String getCargo() {
        return cargo;
    }

    /**
     * Establece el cargo del empleado.
     *
     * @param cargo Nuevo cargo del empleado.
     */
    public void setCargo(String cargo) {
        this.cargo = cargo;
    }

    /**
     * Obtiene el salario del empleado.
     *
     * @return Salario del empleado.
     */
    public double getSalario() {
        return salario;
    }

    /**
     * Establece el salario del empleado.
     *
     * @param salario Nuevo salario del empleado.
     */
    public void setSalario(double salario) {
        this.salario = salario;
    }

    /**
     * Devuelve una representación de cadena del objeto Empleado.
     *
     * @return Cadena que representa al objeto Empleado.
     */
    @Override
    public String toString() {
        return "Empleado{" +
                "nombre='" + nombre + '\'' +
                ", cargo='" + cargo + '\'' +
                ", salario=" + salario +
                '}';
    }
}

/**
 * La clase Empleados gestiona una lista dinámica de objetos Empleado.
 */
public class Empleados {
    private Empleado[] lista;

    /**
     * Constructor de la clase Empleados que inicializa la lista de empleados como vacía.
     */
    public Empleados() {
        lista = new Empleado[0];
    }

    /**
     * Agrega un nuevo empleado a la lista de empleados.
     * 
     * @param nombre nombre del nuevo empleado
     * @param cargo cargo del nuevo empleado
     * @param salario salario del nuevo empleado
     */
    public void altaEmpleado(String nombre, String cargo, double salario) {
        Empleado nuevoEmpleado = new Empleado(nombre, cargo, salario);
        Empleado[] nuevaLista = new Empleado[lista.length + 1];
        for (int i = 0; i < lista.length; i++) {
            nuevaLista[i] = lista[i];
        }
        nuevaLista[lista.length] = nuevoEmpleado;
        lista = nuevaLista;
    }

    /**
     * Aumenta el salario de todos los empleados en la lista por un porcentaje dado.
     * 
     * @param porcentaje porcentaje de aumento del salario
     */
    public void aumentarSalario(double porcentaje) {
        for (Empleado empleado : lista) {
            double nuevoSalario = empleado.getSalario() * (1 + porcentaje / 100);
            empleado.setSalario(nuevoSalario);
        }
    }

    /**
     * Muestra los detalles de todos los empleados en la lista.
     */
    public void mostrarEmpleados() {
        for (Empleado empleado : lista) {
            System.out.println(empleado);
        }
    }
}



![capturabuena](https://github.com/CarlosMurilloC/Parcial2/assets/158159694/f8d3399b-8819-470e-8d94-2004dfc8c5ac)





