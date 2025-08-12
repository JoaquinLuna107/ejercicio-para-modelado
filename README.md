public class Main {

    public static class Medico {
        private int idMedico;
        private String nombre;
        private String matricula;

        public int getIdMedico() {
            return idMedico;
        }
        public void setIdMedico(int idMedico) {
            this.idMedico = idMedico;
        }

        public String getNombre() {
            return nombre;
        }
        public void setNombre(String nombre) {
            this.nombre = nombre;
        }

        public String getMatricula() {
            return matricula;
        }
        public void setMatricula(String matricula) {
            this.matricula = matricula;
        }

        public static class Paciente {
            private int idPaciente;
            private String nombre;
            private int numerotelefono;
            private String email;

            public int getIdPaciente() {
                return idPaciente;
            }
            public void setIdPaciente(int idPaciente) {
                this.idPaciente = idPaciente;
            }

            public String getNombre() {
                return nombre;
            }
            public void setNombre(String nombre) {
                this.nombre = nombre;
            }

            public int getNumerotelefono() {
                return numerotelefono;
            }
            public void setNumerotelefono(int numerotelefono){
                this.numerotelefono = numerotelefono;
            }

            public String getEmail() {
                return email;
            }
            public void setEmail(String email) {
                this.email = email;
            }
        }

        public static class Medicamento {
            private int idMedicamento;
            private String nombre;
            private int stockDisponible;
            private boolean requiereReceta;

            public int getIdMedicamento() {
                return idMedicamento;
            }
            public void setIdMedicamento(int idMedicamento) {
                this.idMedicamento = idMedicamento;
            }

            public String getNombre() {
                return nombre;
            }
            public void setNombre(String nombre) {
                this.nombre = nombre;
            }

            public int getStockDisponible() {
                return stockDisponible;
            }
            public void setStockDisponible(int stockDisponible) {
                this.stockDisponible = stockDisponible;
            }

            public boolean isRequiereReceta() {
                return requiereReceta;
            }
            public void setRequiereReceta(boolean requiereReceta) {
                this.requiereReceta = requiereReceta;
            }
        }

        public static class Receta {
            private int idReceta;
            private String fechaEmision;
            private String observacion;
            private Medico medico;
            private Paciente paciente;

            public int getIdReceta() {
                return idReceta;
            }
            public void setIdReceta(int idReceta) {
                this.idReceta = idReceta;
            }

            public String getFechaEmision() {
                return fechaEmision;
            }
            public void setFechaEmision(String fechaEmision) {
                this.fechaEmision = fechaEmision;
            }

            public String getObservacion() {
                return observacion;
            }
            public void setObservacion(String observacion) {
                this.observacion = observacion;
            }

            public Medico getMedico() {
                return medico;
            }
            public void setMedico(Medico medico) {
                this.medico = medico;
            }

            public Paciente getPaciente() {
                return paciente;
            }
            public void setPaciente(Paciente paciente) {
                this.paciente = paciente;
            }
        }
        public static class Reserva {
            private int idReserva;
            private String fecha;
            private String estadoReserva;
            private int cantidad;
            private Medico medico;
            private Medico.Paciente paciente;

            // Getters y setters
            public int getIdReserva() {
                return idReserva;
            }
            public void setIdReserva(int idReserva) {
                this.idReserva = idReserva;
            }

            public String getFecha() {
                return fecha;
            }
            public void setFecha(String fecha) {
                this.fecha = fecha;
            }

            public String getEstadoReserva() {
                return estadoReserva;
            }
            public void setEstadoReserva(String estadoReserva) {
                this.estadoReserva = estadoReserva;
            }

            public int getCantidad() {
                return cantidad;
            }
            public void setCantidad(int cantidad) {
                this.cantidad = cantidad;
            }

            public Medico getMedico() {
                return medico;
            }
            public void setMedico(Medico medico) {
                this.medico = medico;
            }

            public Medico.Paciente getPaciente() {
                return paciente;
            }
            public void setPaciente(Medico.Paciente paciente) {
                this.paciente = paciente;
            }
        }

    }

    public static void main(String[] args) {

        //====Parte de Medico====
        Medico medico1 = new Medico();
        medico1.setIdMedico(123);
        medico1.setNombre("Joaquin Luna");
        medico1.setMatricula("MAT-777");

        System.out.println("=== Medico ===");
        System.out.println("ID Médico: " + medico1.getIdMedico());
        System.out.println("Nombre: " + medico1.getNombre());
        System.out.println("Matrícula: " + medico1.getMatricula());

        // Parte de Paciente
        Medico.Paciente paciente1 = new Medico.Paciente();
        paciente1.setIdPaciente(195);
        paciente1.setNombre("Mateo Pedretti");
        paciente1.setNumerotelefono(354123772);
        paciente1.setEmail("Mathew10@gmail.com");

        System.out.println("\n\n=== Paciente ===");
        System.out.println("El Id del paciente es: " + paciente1.getIdPaciente());
        System.out.println("Nombre del paciente :" + paciente1.getNombre());
        System.out.println("Numero de Telefono :" + paciente1.getNumerotelefono());
        System.out.println("Email :" + paciente1.getEmail());

        //==== Parte de Medicamento====
        Medico.Medicamento medicamento1 = new Medico.Medicamento();
        medicamento1.setIdMedicamento(456);
        medicamento1.setNombre("paracetamol");
        medicamento1.setStockDisponible(34);
        medicamento1.setRequiereReceta(true);

        System.out.println("\n\n=== Medicamento ===");
        System.out.println("Id Medicamento: " + medicamento1.getIdMedicamento());
        System.out.println("Nombre: " + medicamento1.getNombre());
        System.out.println("Stock disponible: " + medicamento1.getStockDisponible());
        System.out.println("Requiere receta: " + medicamento1.isRequiereReceta());

        // Parte de Receta
        Medico.Receta receta1 = new Medico.Receta();
        receta1.setIdReceta(34);
        receta1.setFechaEmision("12-08-25");
        receta1.setObservacion("Debe de tomar una pildora cada 8 horas por 3 dias");
        receta1.setMedico(medico1);      // PASAR el objeto medico1
        receta1.setPaciente(paciente1);  // PASAR el objeto paciente1

        System.out.println("\n\n=== Receta ===");
        System.out.println("ID Receta: " + receta1.getIdReceta());
        System.out.println("Fecha Emisión: " + receta1.getFechaEmision());
        System.out.println("Observación: " + receta1.getObservacion());
        System.out.println("Médico: " + receta1.getMedico().getNombre());
        System.out.println("Paciente: " + receta1.getPaciente().getNombre());

        // Parte de Reserva

        // Parte de Reserva
        Medico.Reserva reserva1 = new Medico.Reserva();

        reserva1.setIdReserva(12);
        reserva1.setFecha("12-08-2025");
        reserva1.setEstadoReserva("Pendiente");
        reserva1.setCantidad(3);
        reserva1.setMedico(medico1);
        reserva1.setPaciente(paciente1);

        System.out.println("\n\n=== Reserva ===");
        System.out.println("ID Reserva: " + reserva1.getIdReserva());
        System.out.println("Fecha: " + reserva1.getFecha());
        System.out.println("Estado: " + reserva1.getEstadoReserva());
        System.out.println("Cantidad: " + reserva1.getCantidad());
        System.out.println("Médico: " + reserva1.getMedico().getNombre());
        System.out.println("Paciente: " + reserva1.getPaciente().getNombre());

    }
}
