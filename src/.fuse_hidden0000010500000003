import java.awt.*;    //importing Libraries for creating game
import java.awt.event.*;
import javax.swing.*;

public class TicTacToe {
    int boardWidth = 600;
    int boardHeight = 650;  //50px for text on Top Panel

    JFrame frame = new JFrame("Tic-Tac-Toe");
    JLabel textlabel = new JLabel();
    JPanel textpanel = new JPanel();
    JPanel boardPanel = new JPanel();
    boolean gameOver = false;
    int turns = 0;

    JButton board[][] = new JButton[3][3];
    String playerX = "X";
    String playerO = "O";
    String currentPlayer = playerX;

    TicTacToe(){ //Constructor called
        frame.setVisible(true);
        frame.setSize(boardWidth,boardHeight);
        frame.setResizable(false);
        frame.setLocationRelativeTo(null);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setLayout(new BorderLayout());

        textlabel.setBackground(Color.DARK_GRAY);
        textlabel.setForeground(Color.white);
        textlabel.setFont(new Font("Arial", Font.BOLD, 50));
        textlabel.setHorizontalAlignment(JLabel.CENTER);
        textlabel.setText("Tic-Tac-Toe");
        textlabel.setOpaque(true);
        
        textpanel.setLayout(new BorderLayout());
        textpanel.add(textlabel);
        frame.add(textpanel,BorderLayout.NORTH);

        boardPanel.setBackground(Color.darkGray);
        boardPanel.setLayout(new GridLayout(3,3));
        frame.add(boardPanel);

        for(int r =0; r<3; r++){
            for(int c=0; c<3; c++){
                JButton tile = new JButton();
                board[r][c] = tile;
                boardPanel.add(tile);

                tile.setBackground(Color.DARK_GRAY);
                tile.setForeground(Color.white);
                tile.setFont(new Font("Arial",Font.BOLD,120));
                // tile.setText(currentPlayer);
                tile.setFocusable(false);

                tile.addActionListener(new ActionListener() {
                    public void actionPerformed(ActionEvent e){
                        if(gameOver)return ;
                        JButton tile = (JButton)e.getSource();
                        if(tile.getText() == ""){
                        tile.setText(currentPlayer);
                        turns++;
                        checkWinner();
                        if(!gameOver){
                        currentPlayer = currentPlayer == playerX ? playerO:playerX;
                        textlabel.setText(currentPlayer + "'s turn");  
                        }                          
                        }
                    }
                });
            }
        }
    }
    void checkWinner(){
        //horizontal
        for(int r =0;r<3;r++){
           if(board[r][0].getText() == "") continue;
           if(board[r][0].getText() == board[r][1].getText() &&
           board[r][1].getText() == board[r][2].getText()){
            for(int i = 0;i<3;i++){
                setWinner(board[r][i]);
            }
                 gameOver= true; 
                 return;
           }   
        }
        //vertical
         for(int c =0;c<3;c++){
           if(board[0][c].getText() == "") continue;
           if(board[0][c].getText() == board[1][c].getText() &&
           board[1][c].getText() == board[2][c].getText()){
            for(int i = 0;i<3;i++){
                setWinner(board[i][c]);
            }            
           gameOver= true;
           return;
           }
        }
        //diagonally
        if(board[0][0].getText()==board[1][1].getText() &&
        board[1][1].getText() == board[2][2].getText()&&
        board[1][1].getText() != ""){
            for(int i =0;i<3;i++){
                setWinner(board[i][i]);
            }
            gameOver= true;
            return;           
        }
        // Anti- diagonal
        if(board[0][2].getText()==board[1][1].getText() &&
        board[1][1].getText() == board[2][0].getText() &&
        board[1][1].getText() != ""){
            for(int i =0;i<3;i++){
                setWinner(board[i][2-i]);
            }
            gameOver= true;
            return;           
        }
        if(turns == 9){
            for(int r =0 ;r<3;r++){
                for(int c =0;c<3;c++){
                    setTie(board[r][c]);
                }
            }
            gameOver = true;
        }        
    }
    void setWinner(JButton tile){
        tile.setBackground(Color.gray);
        tile.setForeground(Color.green);
        textlabel.setText(currentPlayer + " is the Winner!");
    }
    void setTie(JButton tile){
        tile.setForeground(Color.orange);
        tile.setBackground(Color.gray);
        textlabel.setText( "Draw!");
    }
}
