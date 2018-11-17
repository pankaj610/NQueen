package algo;

public class NQueen {

    static int total = 0;

    static void NQueen(int[][] board, int row) {
//        if(row+1==board.length){return;}

        if (row == board.length) {
//                    System.out.println("yes");
            print(board);
            total++;
            return;
        }

        for (int col = 0; col < board.length; col++) {

//            System.out.println(row+"--"+col);
            if (isSafe(board, row, col)) {
                board[row][col] = 1;
                NQueen(board, row + 1);

                board[row][col] = 0;
            }
        }
    }

    static boolean isSafe(int[][] board, int row, int col) {
        for (int i = 0; i < row; i++) {
            if (board[i][col] == 1) {
                return false;
            }
        }
        int i = row;
        int j = col;
        while (i >= 0 && j >= 0) {
            if (board[i][j] == 1) {
                return false;
            }
            i--;
            j--;
        }
        i = row;
        j = col;
        while (i >= 0 && j < board.length) {
            if (board[i][j] == 1) {
                return false;
            }
            i--;
            j++;
        }
        return true;
    }

    static void print(int[][] board) {
        for (int i = 0; i < board.length; i++) {
            for (int j = 0; j < board[i].length; j++) {
                System.out.print(board[i][j] + " ");
            }
            System.out.println();
        }
        System.out.println("--------");

    }

    public static void main(String[] args) {
        int[][] board = new int[8][8];
//        print(board);
//        board[0][0] = 1;
//        System.out.println(isSafe(board, 1, 1));
        NQueen(board, 0);
        System.out.println("Total : " + total);
    }
}
