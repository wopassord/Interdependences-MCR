En este habita la clase "Scheduler" este es el cerebro que se encarga de comunicarse con todos los motores, recibe el delta de tiempo pasado entre la simulación y el tiempo real del clock interno del update del bml_scheduler_behavior y va disparando aquellos comandos que estén en la cola de "Signals" según el tiempo que haya transcurrido para hacer una simulación que vaya a tiempo real. 

