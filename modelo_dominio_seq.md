@startuml
class Paciente {
  +ID: int
  +Nome: string
  +Idade: int
}

class DispositivoIoT {
  +ID: int
  +Modelo: string
  +Sensor: string
}

class MedicaoTemperatura {
  +ID: int
  +Valor: float
  +DataHora: datetime
  +Status: string
}

class PlataformaIoT {
  +ID: int
  +Nome: string
  +URL: string
}

class Notificacao {
  +ID: int
  +Mensagem: string
  +DataHora: datetime
}

Paciente "1" -- "0..*" MedicaoTemperatura
DispositivoIoT "1" -- "0..*" MedicaoTemperatura
MedicaoTemperatura "1" -- "1" PlataformaIoT
PlataformaIoT "1" -- "0..*" Notificacao
@enduml
