#Taller 1
#Estudiante Jonathan Gutiérrez


""" Para este proyecto se nos propone que hagamos una actualizacion de un sistema para actualizar el 
    calculo de las eras de las piedras por medio de una formula con la libreria math, """
import math

contador=1
#Ingresa el numero de muestras con la siguiente instruccion
Muestras=int(input("Digite la cantidad de muestras a estudiar :"))
#ciclo repetitivo for, con el fin de repetir el numero de muestras segun lo 
#solicitado por el usuario


for contador in range(Muestras):
    contador =contador+1
    #Imprime dentro del ciclo el numero de muestra
    print("Ingrese los datos de la muestra "+ str(contador))

    try:# try de validacion de los datos digitados por el usuario correctamente
        
        edad = float(input("Digite la cantidad de la masa:"))
        argon = float(input("Digite la cantidad a argon:"))
           
        print ("***Datos ingresados  correctamente***")
        
        

        #Formula de Calculo de la edad de la piedra    
        
        Result = edad*1.248*math.log(3)


        #Impresiones de cada muestra
        print("el numero de la muestra es:")
        print(contador)
        print ( "La cantidad de masa es:")
        print(edad)
        print("La edad aproximada es:")
        print(Result)
        print()
        if (Result < 65.5):
            print ("La era es Cenozoica")
        else:
            if Result <251:
                print ("La era es Mezosoica")
            else:
                if Result < 542:
                    print ("La era es paleozoica")
                else:
                     print ("La era es pre paleozoica")

        
    except:# en el caso que los datos no sean ingresados correctamente se encicla en
        #este punto hasta que el usuario los digite correctamente 
        
        print ("***Datos incorrectos vuelva a ingresarlos*** ")
        
        edad = float(input("Digite la cantidad de la masa:"))
       #Formula de Calculo de la edad de la piedra 
        Result = edad*1.248*math.log(3)
        #Impresiones de la piedra al corregir los datos 
        print("El numero de la muestra es:")
        print(contador)
        print("La edad aproximada es:")
        print(Result)
        print()
        if (Result < 65.5):
            print ("La era es Cenozoica")
        else:
            if Result < 251:
                print ("La era es Mezosoica")
            else:
                if Result <  542:
                    print ("La era es paleozoica")
                else:
                     print ("La era es prepaleozoica")

