# project-superheroes
abstract class ProjectX {
    // Abstract method to be implemented by subclasses
    private String name;
    private String power;
    final String universe = "earth dc-69";

    ProjectX(String name, String power) {// Constructor parameters
        this.name = name;
        this.power = power;
    }

    public String getName() {// Getter method for name
        return name;

    }

    public String getPower() {// Getter method for power
        return power;
    }

    abstract void fightt();// Abstract method for fighting

    void displayInfo() {// Method to display information
        System.out.println("Name: " + name + ", Power: " + power + ", Universe: " + universe);
    }

    void fightt(String villian) {// Overloaded method for fighting with an opponent
        System.out.println(name + " is fighting against " + villian);
    }
}

interface ability {// interface for abilities and skills
    void fly();

    void run();// Interface methods for abilities
}

class Batmann extends ProjectX implements ability {

    // Subclass extending ProjectX and implementing ability interface
    public Batmann(String name, String power) {// Constructor
        super(name, power);
    }

    void fightt() {// Implementing abstract method
        System.out.println("batman fights with his intelligence and gadgets" + getName());
    }

    public void fly() {// Implementing interface method
        System.out.println("batman cannot fly but uses his glider to soar through the skies" + getName());
    }

    public void run() {// Implementing interface method
        System.out.println("batman is an exceptional runner and can chase down criminals on foot" + getName());
    }

    void fightt(String villian) {// Overloaded method implementation
        System.out.println(getName() + " is fighting against " + villian);
    }
}

class daredevill extends ProjectX implements ability {

    // Subclass extending ProjectX and implementing ability interface
    public daredevill(String name, String power) {// Constructor for daredevill
        super(name, power);
    }

    void fightt() {// Implementing abstract method
        System.out.println("daredevill fights using his heightened senses and martial arts skills");
    }

    public void fly() {// Implementing interface method
        System.out.println(
                "daredevill cannot fly but uses his acrobatic skills and billy clubs to navigate the city" + getName());
    }

    public void run() {
        System.out.println(
                "daredevill is an agile runner and can swiftly move through the streets of hell's kitchen" + getName());
    }

    void fightt(String villian) {// Overloaded method implementation
        System.out.println(getName() + " is fighting against " + villian);
    }

    public class projecty {
        public static void main(String[] args) {
            Batmann bt = new Batmann("batman", "batman's gadgets");
            bt.displayInfo();
            bt.fightt();// Calling methods
            bt.fly();
            bt.run();
            bt.fightt("joker");// Calling overloaded method

            daredevill d = new daredevill("darevil", "daredevill's sonar skills");// Creating daredevill object
            d.displayInfo();
            d.fightt();
            d.fly();
            d.run();
            d.fightt("kingpin");// Calling overloaded method

        }
    }
}
