## Welcome :)

Welcome to my portfolio website.

My name is Bryan Carty. I'm currently a computer science student at the University Of Limerick.

Below, you will find my skills, interests and the projects I've partook in during my academic career. 
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

- Completing road warden course

- Qualifying to represent my school at Connacht cross country running

- Getting on my schools top 10 fittest list after running 107 lengths in the annual bleap fitness test

- Being picked to be a buddy to a group of incoming first year students during secondary school

### Top 5 Projects
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

Project2: Non Profit Organization Website.

Brief: Develop a website for a Non Profit Organization with a donate page and suitable contact resource.

Technical Skills Required:

- HTML

- CSS

- JavaScript

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
            <p style="margin:0 auto; font-size:20px; max-width:500px">One and a half acres of forest is cut down every second. At this rate, it is estimated that within 100 years there will be no rainforests left.<br><br>
            By donating, you are enabling our team to plant trees where reforestation is needed the most.
            For every €1 donated, one tree is planted.<br><br>
            Join us on our mission to plant 300 million trees by the year 2025.
            </p>
        </div>
```







