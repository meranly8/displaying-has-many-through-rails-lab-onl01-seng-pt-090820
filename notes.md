# Doctor
    name
    department

    has_many :appointments
    has_many :patients, through: :appointments

    rails g model Doctor name:string department:string --no-test-framework --skip-routes 

## Doctor#show

# Appointment
    patient_id
    doctor_id
    appointment_datetime
        January 12, 2016 at 3:00

    belongs_to :doctor
    belongs_to :patient

    rails g model Patient name:string age:integer --no-test-framework --skip-routes 

## Appointment#show

# Patient
    name
    age

    has_many :appointments
    has_many :doctors, through: :appointments

    rails g model Appointment appointment_datetime:datetime doctor:belongs_to patient:belongs_to --no-test-framework --skip-routes 

## Patient#show
## Patient#index