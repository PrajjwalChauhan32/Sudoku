# Sudoku
Insert elements in Sudoku and validate them to solve it.
// Java Sudoku Project

public class PlaySudoku {

	public static void main(String[] args) {
		// How to give input
		// How to quit
		// Asking user to choose level
		// Creating Sudoku object of that level
		// Calling playSudoku method
		
		Sudoku s = new Sudoku(level);
		
		s.playSudoku();

	}

}

public class Sudoku {

	private int[][] sudokuBoardEasy = {{ 1, 2, 9, 6, 5, 3, 4, 7, 8 },
			  						   { 8, 4, 5, 7, 9, 1, 2, 6, 3 },
			  						   { 3, 6, 7, 8, 2, 4, 5, 9, 1 },
			  						   { 4, 8, 6, 3, 1, 2, 7, 5, 9 },
			  						   { 5, 3, 1, 4, 7, 9, 6, 8, 2 },
			  						   { 7, 9, 2, 5, 8, 6, 3, 1, 4 },
			  						   { 2, 7, 8, 1, 4, 5, 9, 3, 6 },
			  						   { 6, 5, 4, 9, 3, 8, 1, 2, 7 },
			  						   { 0, 0, 3, 2, 0, 0, 0, 4, 5 }};
	
	private int[][] sudokuBoardMedium = {{1, 2, 0, 0, 0, 3, 4, 0, 0},
	   		 							 {0, 4, 5, 0, 0, 0, 2, 6, 0},
	   		 							 {0, 0, 7, 8, 0, 0, 0, 9, 1},
	   		 							 {0, 0, 0, 3, 1, 0, 0, 0, 9},
	   		 							 {0, 0, 0, 0, 7, 0, 0, 0, 0},
	   		 							 {7, 0, 0, 0, 8, 6, 0, 0, 0},
	   		 							 {2, 7, 0, 0, 0, 5, 9, 0, 0},
	   		 							 {0, 5, 4, 0, 0, 0, 1, 2, 0},
	   		 							 {0, 0, 3, 2, 0, 0, 0, 4, 5}};
	
	private int[][] sudokuBoardHard = {{6, 0, 0, 0, 4, 0, 0, 0, 0},
									   {9, 0, 0, 0, 0, 5, 6, 0, 1},
									   {1, 0, 0, 0, 7, 0, 3, 0, 0},
									   {0, 0, 0, 0, 0, 0, 0, 6, 4},
									   {0, 3, 0, 0, 0, 4, 0, 2, 0},
									   {0, 8, 0, 0, 2, 0, 5, 0, 0},
									   {0, 0, 0, 0, 0, 0, 0, 0, 0},
									   {3, 0, 0, 9, 0, 0, 2, 0, 0},
									   {0, 7, 0, 0, 5, 0, 1, 0, 0}};
	
	public Sudoku(int level) {
		this.level = level;
		setSudokuBoard();
	}
	
	public void setSudokuBoard() {
		// set SudokuBoard according to level chosen by user
	}
	
	public void playSudoku() {
		// getting the in built slot positions(row, column) to differentiate between in built slots and user inputs -> getInBuiltSlots();
		// displaying the initial configuration of the Sudoku -> displaySudoku();
		// while the puzzle is not complete:
			// add numbers to Sudoku -> addNumbersToSudoku();
			// display resulting Sudoku -> displaySudoku();
		// Completion message when finished
	}

	public void getInBuiltSlots() {
		// storing the positions of the in built slots in a list of integer array

	}
	
	public void displaySudoku() {
		// displaying the Sudoku in a particular format
		// printing in built slots in black color
		// printing user defined numbers in blue
	}
	
	public boolean isComplete() {
		// checking if puzzle has blank spaces or not
	}
	
	public void addNumbersToSudoku() {
		// taking input from the user in the form: Row Column Number
		// if input is Q or q 
			// exit program
		// if row, column and number is valid -> isValidSlot();
			// add number to sudoku
	}
	
	public boolean isValidSlot(int row, int column, int number) {
		return (isValidRow(row)) &&  
			(isValidColumn(column)) &&
			(isValidNumber(number)) &&
			(!isSlotInBuilt(row, column)) && 
			(!isNumberInRow(row, number))  &&
			(!isNumberInColumn(column, number)) &&
			(!isNumberInLocalGrid(row, column, number));
	}
	
	public boolean isValidRow(int row) {
		// checking if row number is in between 1 and 9
		// if invalid
			// Error message: Invalid row
	}
	
	public boolean isValidColumn(int column) {
		// checking if column number is in between 1 and 9
			// if invalid
				// Error message: Invalid column
	}
	
	public boolean isValidNumber(int number) {
		// checking if number is in between 1 and 9
		// if invalid
			// Error message: Invalid number
	}
	
	public boolean isSlotInBuilt(int row, int column) {
		// checking if the position in which user wants to input is inbuilt or not
		// if inbuilt slot
			// Error message: cannot change initial configuration
	}
	
	public boolean isNumberInRow(int row, int number) {
		// checking if the number is already present in the row
		// if present
			// Error message: number already present in row
	}
	
	public boolean isNumberInColumn(int column, int number) {
		// checking if the number is already present in the column
		// if present
			// Error message: number already present in column
	}
	
	public boolean isNumberInLocalGrid(int row, int column, int number) {
		// checking if the number is already present in the local 3x3 grid
		// if present
			// Error message: number already present in local 3x3 grid
	}
	
}

