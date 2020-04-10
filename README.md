## Welcome :)

Welcome to my portfolio website.

My name is Bryan Carty. I'm currently a computer science student at the University Of Limerick.

Below, you will find details of my skills, interests and the projects I participated in during my academic career. 



### Personal Statement

I like to pride myself on being a highly motivated and hardworking individual. Such traits can be seen in my excellent exam results.

Junior Cert results: (7A'S,3B'S,1C). Note: These were the best results in my school that year.

Leaving Cert results: (556 points). Note: These were the third best results in my school that year.

I look forward to continuing the same degree of academic success throughout my third level education.

My eventual career goal is to become a fully-qualified and experienced software developer, with the longer-term aspiration of starting my own business.



### Interests

- Coding

- Running

- Going To The Gym

- Reading

- The Stock Market



### Achievements

- 1st Home, Carol Kelly Memorial Run

- 1st Home U18, Kilkerrin 10k

- 1st Place, Senior regional Essay Competition

- Exam Results (Outlined Above)

- Student Of The Year

- Completeing level 1 Acquatics Coaching Course

- Competeing at National Division 1 Swimming
Note: To get to this level involved a lot of training, including waking up at 5am to train before school.

- Completing road warden course

- Qualifying to represent my school at Connacht cross country running

- Getting on my schools top 10 fittest list after running 107 lengths in the annual bleap fitness test

- Being picked to be a buddy to a group of incoming first year students during secondary school



### Volunteering

I have volunteered at community events in the past such as Ballygar Annual Carnival. 

During my time in competitive swimming I volunteered as a time keeper at some events.



### 5 Sample Projects

Project 1: Develop a spreadsheet system.

Brief: Develop a Java class (or classes, if necessary) to allow sheet names to be managed as a list of names.

Technical Skills Required:

- Java

Snippet:
```markdown

public static String remove(int index) {
//Data Description
	String output="";
//Algorithm Description	
	for(int loop=0; loop<spreadsheet.length; loop++) {
		if((index-1)==loop&&positionCounter>1){
			for(int l=loop; l<spreadsheet.length-1; l++) {
				spreadsheet[l]=spreadsheet[l+1];
			}
			positionCounter--;
			spreadsheet[spreadsheet.length-1]=new String();
			output = spreadsheet[loop];
		}	
	}
	return output;
}



public static int move(String from, String to, boolean before) {
//Data Description
	SpreadsheetUtilityMethods UtilityMethodsObject = new SpreadsheetUtilityMethods();
	boolean inList1 = UtilityMethodsObject.onList(spreadsheet, from);
	boolean inList2 = UtilityMethodsObject.onList(spreadsheet, to);
	int indexFrom = UtilityMethodsObject.indexOf(spreadsheet, from);
	int indexTo = UtilityMethodsObject.indexOf(spreadsheet, to);
	String temp = spreadsheet[indexFrom];
	int output = -1;
//Algorithm Description
	if(from!=to && inList1==true && inList2==true) {
		if(before==true) {
			for(int loop = indexFrom; loop<indexTo-1; loop++) {
				spreadsheet[loop]=spreadsheet[loop+1];
			}
			spreadsheet[indexTo-1]=temp;
			output = indexTo-1;
		}else {
			for(int loop = indexFrom; loop<indexTo; loop++) {
				spreadsheet[loop]=spreadsheet[loop+1];
			}
			spreadsheet[indexTo]=temp;
			output = indexTo;
		}
	}
	return output;
}

```



Project 2: Non Profit Organization Website.

Brief: Develop a website for a Non Profit Organization with a donate page and suitable contact resource.

Technical Skills Required:

- HTML

- CSS

- JavaScript

- Team Work

Snippet:
```markdown
<header>
        <div class="container">
            <img src="Assets/GreenWillLogo.png" height="50px" width="600px" alt = logo class="logo">
            <nav>
                <ul>
                    <li> <a href="HomePage.html">HOME</a> </li>
                    <li> <a href="AboutPage.html">ABOUT</a> </li>
                    <li> <a href="ContactPage.html">CONTACT</a> </li>
                    <li> <a href="DonatePage.html">DONATE</a></li>    
                </ul>
            </nav>
        </div>
    </header>
    <section>
        <div class="boxes">
            <img class="w-image"src="Assets/plantingtree.jpg"alt="Father & Son Planting A Tree"style="width:560px;height:auto;">
            <br>
            <p style="margin:0 auto; font-size:20px; max-width:500px">One and a half acres of forest is cut down every second. At this 	             rate, it is estimated that within 100 years there will be no rainforests left.<br><br>
            By donating, you are enabling our team to plant trees where reforestation is needed the most.
            For every €1 donated, one tree is planted.<br><br>
            Join us on our mission to plant 300 million trees by the year 2025.
            </p>
        </div>
```



Project 3: Random Wordsearch Generator.

Brief: Develop a class that will be used to generate puzzles using a two-dimensional grid.

Technical Skills Required: 

- Java

Snippet:
```markdown

public WordSearchPuzzle(String wordFile, int wordCount, int shortest, int longest){
        puzzleWords=loadWordsFromFile(wordFile);
        List<String> newWords = new ArrayList<String>(wordCount);
        for(int counter = 0; counter<wordCount; counter++){
            int randomNum = (int)(Math.random()*puzzleWords.size());
            String randWord = puzzleWords.get(randomNum);
            if(randWord.length()>=shortest&&randWord.length()<=longest&&newWords.contains(randWord)==false){
                newWords.add(randWord);
            }else{
                counter--;
            }
        }
        puzzleWords=newWords;
        generateWordSearchPuzzle();
    }    

    private static ArrayList<String> loadWordsFromFile(String fileName){
        try{
            FileReader aFileReader = new FileReader(fileName);
            BufferedReader aBufferReader = new BufferedReader(aFileReader);
            ArrayList<String> words = new ArrayList<String>();
            String aWord;
            aWord = aBufferReader.readLine();
            while(aWord!=null){
                words.add(aWord.toUpperCase());
                aWord=aBufferReader.readLine();
            }
            aBufferReader.close();
            aFileReader.close();
            return words;
        }catch(IOException x){
            return null;
        }
    }

    public List<String> getWordSearchList(){
        return puzzleWords;
    }
    
    private void generateWordSearchPuzzle(){
        helperClassObject.gridDimensions(puzzleWords);
        List<String> rightHorizontalWords=helperClassObject.horizontalRightWords();
        List<String> leftHorizontalWords=helperClassObject.horizontalLeftWords();
        List<String> upVerticalWords=helperClassObject.verticalUpWords();
        List<String> downVerticalWords=helperClassObject.verticalDownWords();
        helperClassObject.fillGrid(rightHorizontalWords, leftHorizontalWords, upVerticalWords, downVerticalWords);
        puzzle = helperClassObject.returnGrid();
    }
    
    public char[][] getPuzzleAsGrid(){
        return puzzle;
    }
```



Project 4: Payout Algorithm (Personal Project).

Description: When pursuing a business idea it was necessary that I develop a very specific algorithm. This algorithm would calculate a persons payout by factoring in the persons day of entry into a contract as well as the quantity of contracts purchased.

Technical Skills Required:

- Java

Note: I'm particularly proud of this project because it was the first time I required my knowledge of coding outside of college. It was also necessary that I figured out the maths for this algo before implementing it in code.

Snippet:
```markdown
private void arithmatic() {
//Data Declaration
int totalDNum = (int)dayNum[dayNum.length-1];
int totalDayNum = totalDNum;
int totalDayNumCopy = totalDNum;
this.dayCount = new int[totalDNum];
//Algorithm Description


//interDayRatioArray
	//Data Declaration
	int sumFact=0;
	//Algorithm Description
	while(totalDayNum>0) {
		sumFact +=totalDayNum;
		dayCount[totalDayNum-1]=totalDayNum;	
		totalDayNum--;
	}	
	
	this.interDayRatio = new double[totalDNum];
	for(int i = 0; i<totalDNum; i++) {
		this.interDayRatio[i]=(double)totalDayNumCopy/sumFact;
		totalDayNumCopy--;
	}
	
	newInterDayRatio();
	
	this.interByPaid = new double[this.numWinningEntries];
	for(int k = 0; k<this.interByPaid.length; k++) {
		this.interByPaid[k]=(double)this.contractWorthBought[k]*this.interDayRatioPerPerson[k];
		sumOfStepThree+=interByPaid[k];
	}
	stepFour = new double[numWinningEntries];
	for(int f = 0; f<numWinningEntries; f++) {
		stepFour[f] = (double)interByPaid[f]/sumOfStepThree;
	}
	for(int y =0; y<numWinningEntries; y++) {
		sumOfAmountWinnersPaid+=contractWorthBought[y];
	}
	amountToBeDispersed = totalMoneyReceived-sumOfAmountWinnersPaid;
	amountDispersedPerPerson = new double[numWinningEntries];
	for(int i = 0; i<numWinningEntries; i++) {
		amountDispersedPerPerson[i]=amountToBeDispersed*stepFour[i];
	}
	totalReturnedPerPerson = new double[numWinningEntries];
	for(int z = 0; z<numWinningEntries; z++) {
		totalReturnedPerPerson[z]=contractWorthBought[z]+amountDispersedPerPerson[z];
	}
	initialPricePerContract = new double[numWinningEntries];
	postPricePerContract = new double[numWinningEntries];
	for(int t=0; t<numWinningEntries; t++) {
		initialPricePerContract[t]=contractWorthBought[t]/contractWorthBought[t];//Assumes all contracts worth 1 euro.
		postPricePerContract[t]=totalReturnedPerPerson[t]/contractWorthBought[t];//as 1 euro also number of contracts.
	}
	percentGain = new double[numWinningEntries];
	for(int r = 0; r<numWinningEntries; r++) {
		percentGain[r]=(((double)postPricePerContract[r]-initialPricePerContract[r])/initialPricePerContract[r])*100;
	}
	winnerPercent = (sumOfAmountWinnersPaid/totalMoneyReceived)*100;
	loserPercent = 100.0-winnerPercent;
	display();	
	}
```



Project 5: Rock, Paper, Scissors Game (Personal Project).

Description: This was another project I did outside of college. For no other reason than just for the fun of it.

Technical Skills: 

- Java

Snippet:
```markdown
int compweaponNumber=(int)(Math.random()*3+1);
System.out.println("Choose your weapon (rock,paper or scissors?)");
weapon=input.nextLine();

if(compweaponNumber==1){
	compWeapon="rock";
}
else if(compweaponNumber==2){
	compWeapon="paper";
	}
else if(compweaponNumber==3){
	compWeapon="scissors";
}
```










