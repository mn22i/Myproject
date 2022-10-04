# Myproject
this is test repo
this repo is created by Amani ALzhrani
C# program
 internal class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Enter how many A person");
            int n=int.Parse(Console.ReadLine());
            Person[] arr = new Person[n];
            for(int i=0;i< n; i++)
            {
                arr[i] = new Person();
                Console.Write("Enter Person{0}Name", i + 1);
                arr[i].Getsetname = Console.ReadLine();
                Console.Write("Enter Person{0}Age", i + 1);
                arr[i].getsetage = int.Parse(Console.ReadLine());
            }
            Console.WriteLine("------Summary------");
            Person.DisplayInfo(arr);
            Console.WriteLine("------Summary after edit------");
            arr[0].Getsetname= "Amoni";
            Person.DisplayInfo(arr);
            Console.ReadLine();
        }
    }
 //   class
 internal class Person
    {
        private string name;
        private int age;

        public  Person(){
            name = "Amoni";
            age = 20;
           }

    public  Person(string n,int a ){
            this.name=n;
            this.age = a;
           }
        public string 
            Getsetname
        {

            get { return name;
            
            }
            set
            {

                name = value;
            }
        }
        public int getsetage
        {
            get
            {
                return age;
            }
            set { age = value; }


        }
        public static void DisplayInfo(Person[] arr)
        {

            foreach(Person p in arr)
            
                Console.WriteLine("name  {0} age is{1}",p.name, p.age);
            
        }

    }
