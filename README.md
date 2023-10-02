class Car:
 def __init__(self, engine, battery):
 self.engine = engine
 self.battery = battery
 def needs_service(self):
 return self.engine.needs_service() or self.battery.needs_service()
from abc import ABC, abstractmethod
class Engine(ABC):
 @abstractmethod
 def needs_service(self):
 pass
class CapuletEngine(Engine):
 def needs_service(self):
 # Implement CapuletEngine service criteria
 pass
class WilloughbyEngine(Engine):
 def needs_service(self):
 # Implement WilloughbyEngine service criteria
 pass
class SternmanEngine(Engine):
 def needs_service(self):
 # Implement SternmanEngine service criteria
 Pass
class Battery(ABC):
 @abstractmethod
 def needs_service(self):
 pass
class SpindlerBattery(Battery):
 def needs_service(self):
 # Implement SpindlerBattery service criteria
 pass
class NubbinBattery(Battery):
 def needs_service(self):
 # Implement NubbinBattery service criteria
 Pass
from car import Car
from engine import CapuletEngine, WilloughbyEngine, SternmanEngine
from battery import SpindlerBattery, NubbinBattery
class CarFactory:
 @staticmethod
 def create_calliope(current_date, last_service_date, current_mileage,
last_service_mileage):
 engine = CapuletEngine()
 battery = SpindlerBattery()
 return Car(engine, battery)
 @staticmethod
 def create_glissade(current_date, last_service_date, current_mileage,
last_service_mileage):
 engine = WilloughbyEngine()
 battery = SpindlerBattery()
 return Car(engine, battery)
 @staticmethod
 def create_palindrome(current_date, last_service_date, warning_light_on):
 engine = SternmanEngine()
 battery = SpindlerBattery()
 return Car(engine, battery)
 @staticmethod
 def create_rorschach(current_date, last_service_date, current_mileage,
last_service_mileage):
 engine = WilloughbyEngine()
 battery = NubbinBattery()
 return Car(engine, battery)
 @staticmethod
 def create_thovex(current_date, last_service_date, current_mileage,
last_service_mileage):
 engine = CapuletEngine()
 battery = NubbinBattery()
 return Car(engine, battery
