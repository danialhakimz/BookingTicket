#include <stdio.h>
#include <string.h>

struct flight_date {
	int day;
	int month;
	int year;
};

struct flight_time {
	int hour;
	int minute;
};

struct flight_information {
	char flight_num[4];
	struct flight_date date;
	struct flight_time time;
	char gate[2];
} flight_info;


main()
{
	int seat[4][5] = {0};
	int i,j,choice,num_of_seat,empty_seat=0,row,col,x=4,y=5,z=0;
	int booking_id ;
	char name[20];

	strcpy(flight_info.flight_num, "AK65");
	strcpy(flight_info.gate, "G9");
	flight_info.date.day = 25;
	flight_info.date.month = 12;
	flight_info.date.year = 2017;
	flight_info.time.hour = 23;
	flight_info.time.minute = 45;

	printf("------Airline Reservation Menu------\n\n\n");
	printf("Press \"1\" -\tBooking\n");
	printf("Press \"2\" -\tDisplay Seat Layout & Occupancy\n");
	printf("Press \"3\" -\tPrint Booking Ticket\n");
	printf("Press \"4\" -\tExit\n");
	printf("\nEnter your choice > ");
	scanf("%d", &choice);
	printf("\n");

	
	switch (choice)
	{
	case 1:
		printf("No. of seat : ");
		scanf("%d", &num_of_seat);

		for (i=0; i<4; i++)
		{
			for (j=0; j<5; j++)
			{
				if (seat[i][j] == 0)
					empty_seat += 1;
			}
		}
		if (num_of_seat > empty_seat)
		{
			printf("Not enough seats available!\n");
			break;
		}
		else
			booking_id = 101;

		fflush(stdin);
		printf("Please enter your name : ");
		scanf("%19[^\n]s", &name);

		printf("Please enter IC Number : ");
		scanf("%19[^\n]s", &name);

		for (i=0; i<4; i++)
		{
			for (j=0; j<5; j++)
			{
				switch(num_of_seat)
				{
					case 1:
					case 2:
					case 3:
					case 4:
					case 5:
						seat[i][num_of_seat-1] = booking_id;
						break;
					case 6:
						seat[i+1][num_of_seat-5] = booking_id;
						break;
				}
			}
		}

		printf("%d\t", seat[0][0]);
		printf("%d\t", seat[0][1]);
		printf("%d\t", seat[0][2]);
		printf("%d\t", seat[0][3]);
		printf("%d\t\n", seat[0][4]);

		printf("%d\t", seat[1][0]);
		printf("%d\t", seat[1][1]);
		printf("%d\t", seat[1][2]);
		printf("%d\t", seat[1][3]);
		printf("%d\t\n", seat[1][4]);
		printf("%d\n", booking_id);
	break;
	case 2:
		seat[2][0] = 101;
		printf("\tA\tB\tC\tD\tE\n");
		for (row=0; row<4; row++)
		{
			printf("\n%d", row+1);
			for (col=0; col<5; col++)
			{
				printf("\t%d", seat[row][col]);
			}
		}
		break;
	case 3:
		printf("Have A Nice Day !");
		break;
	default:
		printf("Unknown choice , please read the instructions again !");
	}

	printf("\n\n");
}

