#InstanceVariable

#ScreenShots

###Main
![Main](Main.png)

###Olive
![Olive](Olive.png)

###OlivePress
![OlivePress](OlivePress.png)

#Codes

###Main

~~~
package ph.edu.dlsu;

import ph.edu.dlsu.olives.Olive;
import ph.edu.dlsu.ph.edu.dlsu.press.OlivePress;

import java.util.ArrayList;

public class Main {

    public static void main(String[] args) {

        ArrayList<Olive> olives = new ArrayList<Olive>();

        Olive olive;

        olive = new Olive();
        System.out.println(olive.name);
        olives.add(olive);

        olive = new Olive();
        System.out.println(olive.name);
        olives.add(olive);

        olive = new Olive();
        System.out.println(olive.name);
        olives.add(olive);

        OlivePress press = new OlivePress();
        press.getOil(olives);

    }
}
~~~

###Olive

~~~
package ph.edu.dlsu.olives;

public class Olive {

    public String name = "Kalamata";
    public String flavor = "Grassy";
    public long color = 0x000000;
    private int oil = 3;

    public int crush(){

        System.out.println("OUCH!");
        return oil;
    }

}
~~~

###OlivePress

~~~
package ph.edu.dlsu.ph.edu.dlsu.press;

import ph.edu.dlsu.olives.Olive;

import java.util.ArrayList;

public class OlivePress {

    public void getOil(ArrayList<Olive> olives){

        int oil = 0;

        for (Olive olive: olives){

            oil += olive.crush();

        }

        System.out.println("You got " + oil + " units of oil");

    }

}
~~~
