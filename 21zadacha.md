//Задача 21. Напишите программу, которая принимает на вход координаты двух точек и находит расстояние между ними в 3D пространстве.

//A (3,6,8); B (2,1,-7), -> 15.84
//A (7,-5, 0); B (1,-1,9) -> 11.53

Console.WriteLine("Решение задачи 21");

int x1 = Coor("x", "A");
int y1 = Coor("y", "A");
int z1 = Coor("z", "A");
int x2 = Coor("x", "B");
int y2 = Coor("y", "B");
int z2 = Coor("z", "B");

int Coor(string coorName, string pointName)
{
    Console.Write($"Введите координату {coorName} точки {pointName}: ");
    return Convert.ToInt16(Console.ReadLine());
}

double Dec(double x1, double x2, 
                double y1, double y2, 
                double z1, double z2){
  return Math.Sqrt(Math.Pow((x2-x1), 2) + 
                   Math.Pow((y2-y1), 2) + 
                   Math.Pow((z2-z1), 2));
}

double length =  Math.Round (Dec(x1, x2, y1, y2, z1, z2), 2 );

Console.WriteLine($"Расстояние между точками:  {length}");