package week2;

public class GuessNumber {
	public static void main(String[] args) {
		JFrame f=new JFrame();
		JLabel c=new JLabel("Guess a number between 1 and 1000");
		JPanel p1=new JPanel();
		JPanel p2=new JPanel();
		JPanel p3=new JPanel();
		JPanel p4=new JPanel();
		JPanel p5=new JPanel();
		final JTextField a=new JTextField(4);
		JButton b=new JButton("获取随机数");
		JButton b1=new JButton("确定");
		final JTextArea area=new JTextArea();
		a.setSize(100, 100);
		p1.add(c);
		p2.add(a);
		p3.add(b);
		p4.add(b1);
		p5.add(area);
		f.setTitle("猜数字");
		f.setSize(300, 300);
		f.add(p1,BorderLayout.BEFORE_FIRST_LINE);
		f.add(p2,BorderLayout.WEST);
		f.add(p3,BorderLayout.AFTER_LAST_LINE);
		f.add(p4,BorderLayout.AFTER_LINE_ENDS);
		f.add(p5,BorderLayout.CENTER);
		f.setVisible(true);
		b.addActionListener(new ActionListener(){
		//Congratulations.You guessed the number
		public void actionPerformed(ActionEvent e) {
		Random a=new Random();
		num=1+a.nextInt(1000);
		}
		});
		b1.addActionListener(new ActionListener(){
		public void actionPerformed(ActionEvent e1) {
		int i=Integer.parseInt(a.getText());
		if(i>num)
		area.setText("Too high.Try again");
		if(i<num)
		area.setText("Too low.Try again");
		if(i==num)
		area.setText("Congratulations.You guessed the number");
		}
		});
		// TODO Auto-generated method stub
		}
		}


}
