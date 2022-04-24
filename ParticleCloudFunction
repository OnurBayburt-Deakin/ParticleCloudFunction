//Initialise LED variable names
int led_red = D4;
int led_green = D3;
int led_blue = D2;


//Function to control LEDs
int LightUp(String colour)
{
    int click_red = -1;
    int click_green = -1;
    int click_blue = -1;
    
    click_red = strcmp(colour, "red");
    click_green = strcmp(colour, "green");
    click_blue = strcmp(colour, "blue");
    
    if (click_red == 0)
    {
        digitalWrite(led_red, HIGH);
        digitalWrite(led_green, LOW);
        digitalWrite(led_blue, LOW);
        return 1;
    }
    else if (click_green == 0)
    {
        digitalWrite(led_red, LOW);
        digitalWrite(led_green, HIGH);
        digitalWrite(led_blue, LOW);
        return 1;
    }
    else if (click_blue == 0)
    {
        digitalWrite(led_red, LOW);
        digitalWrite(led_green, LOW);
        digitalWrite(led_blue, HIGH);
        return 1;
    }
    else
    {
        digitalWrite(led_red, LOW);
        digitalWrite(led_green, LOW);
        digitalWrite(led_blue, LOW);
        return 0;
    }
}


void setup()
{
    //Initialise output pins
    pinMode(led_red, OUTPUT);
    pinMode(led_green, OUTPUT);
    pinMode(led_blue, OUTPUT);
	
    //Expose function to cloud
    Particle.function("LightUp", LightUp);
}


void loop()
{
}
