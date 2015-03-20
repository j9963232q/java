package test2;
import java.util.Scanner;
public class New2 
{
	public static void main(String[] args) 
	{
		Scanner cin = new Scanner(System.in);
		try
		{
			int number,i;
			number=cin.nextInt();
			while(number>0)
			{
				String name,winer;
				int ppoints=0,wpoints=0,solved=0,wsolved=0,p,pt;
				name=cin.next();
				for(i=0;i<4;i++)
				{
					p=cin.nextInt();
					pt=cin.nextInt();
					if(pt!=0)
					{
						ppoints=ppoints+(p-1)*20+pt;
						solved++;
					}
				}
				if(solved>wsolved)
				{
					winer = name;
					wpoints=ppoints;
					wsolved=solved;
				}
				else if(ppoints<wpoints&&solved==wsolved)
				{
					winer = name;
					wpoints=ppoints;
					wsolved=solved;
				}
				number--;
			}
			System.out.printf("%s %d %d",winer,wsolved,wpoints);
		}
		finally
		{
			cin.close();
		}
			
	}

}
