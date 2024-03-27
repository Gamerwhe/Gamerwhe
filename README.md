using System;

class SoccerGame
{
    static void Main(string[] args)
    {
        Console.WriteLine("Welcome to a Simple Soccer Game!");

        // Get the name of the first player
        Console.Write("Enter the name of the first player: ");
        string player1 = Console.ReadLine();

        // Get the name of the second player
        Console.Write("Enter the name of the second player: ");
        string player2 = Console.ReadLine();

        Console.WriteLine("\nThe match is starting!");
        Console.WriteLine("First half begins!");

        // Simulate the first half
        SimulateHalf(player1, player2);

        Console.WriteLine("\nSecond half begins!");

        // Simulate the second half
        SimulateHalf(player2, player1);

        // Show the match result
        Console.WriteLine("\nThe match is over!");
        Console.WriteLine("Result: {0} 0 - 0 {1}", player1, player2);
    }

    static void SimulateHalf(string team1, string team2)
    {
        Random rand = new Random();

        // Simulate a half of 45 minutes
        for (int minute = 1; minute <= 45; minute++)
        {
            // Generate a random event (e.g., goal or foul)
            int eventOutcome = rand.Next(1, 101); // Generate a random number between 1 and 100

            // Goal scored
            if (eventOutcome <= 5) // 5% chance of a goal in each minute
            {
                Console.WriteLine("GOAL!!! {0} scores at minute {1}!", team1, minute);
            }
            // Foul occurred
            else if (eventOutcome >= 95) // 5% chance of a foul in each minute
            {
                Console.WriteLine("Foul committed at minute {0}!", minute);
            }
        }
    }
}![_37206958-df01-4322-a0b9-27b63305c65c](https://github.com/Gamerwhe/Gamerwhe/assets/165196899/9be17c1e-c42c-4aa5-ab7c-ae6cca0bf851)
