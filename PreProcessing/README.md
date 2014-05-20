========================================================================

1. Getting started
	1.1 Git
	1.2 Project setup in Eclipse
2. Structure
	2.1 File structure
	2.2 Project structure
3. Run
3. Results

========================================================================

1. Getting started
	1.1 Git 
		First of all, you should create an account on https://github.com/
		Then, if you are not familiar with git, you can find a good introduction tutorial at http://try.github.io/levels/1/challenges/1
		In order to download the project, open a shell and go to the desired location. Then, perform a "git clone %REPO_URL", where %REPO_URL is the URL you can find on the right
		when you visualize the git project on github (Under HTTPS clone url).
	1.2 Eclipse
		Once the full repository has been copied to your system, make a copy of the "Preprocessing" folder in Workspace.
		Delete the original "Preprocessing" folder, then launch Eclipse and set the workspace to the workspace/ folder of the archive.
		Create a new Java Project called "Preprocessing", then copy/paste all the files you saved previously in it.
		Refresh Eclipse packets explorer and you should see the files now.
		Finally, you need to link the libraries by right-clicking the project and chosing "Properties" -> "Java Build Path" -> 
		"Add External JARs...". Import commons-io-2.4.jar and standford-postagger (libraries/ folder)
		You are all set, the project should be able to be run.

=========================================================================

2. Structure
	2.1 File structure
		The project folders contains the following : (subfolder_name : content -> [file extension])
			* data : all the data of the project
				* parsed : all the parsed files, a parsed text exists per episode/season/show -> [*.parsed]
				* preprocessed : all the show preprocessed files -> [*.preprocessed]
				* subtitles : all the subtitles files per episodes -> [*.srt]
				(Note: Only few files are uploaded on the git as examples, the full dataset of subtitles can be downloaded with the crawler script.)
			* libraries : all the libs required to run the project
			* workspace 
				* src : code source files
				* taggers : required tagging files
	2.2 Project Structure 
		The project contains, at the moment, 2 main packages : parser and preprocessing.

=========================================================================

3. Run
	The project contains several run configurations, allowing to run each part individually. 
	In each packet, a Run.java class is present and should be runned using
	"Run as..." -> "Java Project".
	If only the subtitles are given and one wants to recompute the sets of preprocessed files, he should first run the parser and then thepreprocessing part.

=========================================================================

4. Results
	The results we are going to use as input for the LDA algorithm are the *.preprocessed show files. 
	Such a file contains a list of words and the number of their occurences, ordered by the latter.

=========================================================================
	
		
	
		
		                                                                                                                                                                                   
