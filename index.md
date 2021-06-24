import java.awt.*;
import java.awt.event.*;
import javax.swing.*;

public class javaGui implements ActionListener {
	
	private static JLabel password1, label;
	private static JTextField username;
	private static JButton button;
	private static JCheckBox radio;
	private static JPasswordField Password;
	
	
public static void main(String[] args)  {
		
		
		// Panel class
		 JPanel panel = new JPanel();
		 panel.setLayout(null);
		
		 
		 // JFrame
		JFrame frame = new JFrame();
		frame.setTitle("LOGIN PAGE");
		frame.setLocation(new Point(500, 300));
		frame.add(panel);
		frame.setSize(new Dimension(400, 200));
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		
		
		// Username label
		label = new JLabel("Username");
		label.setBounds(100, 0, 70, 20);
		panel.add(label);
		
		
		// Username TextField
		username = new JTextField();
		username.setBounds(100, 20, 193, 28);
		panel.add(username);
			
		
		// Password Label
		password1 = new JLabel("Password");
		password1.setBounds(100, 45, 70, 20);
		panel.add(password1);
		
		
		// Password TextField
		Password = new JPasswordField();			  			 
		Password.setBounds(100, 65, 193, 28);
		panel.add(Password);
		
		// Button component
		button = new JButton("Login");
		button.setBounds(100, 105, 97, 25);
		button.setForeground(Color.WHITE);
		button.setBackground(Color.BLACK);
		button.addActionListener((ActionListener) new javaGui());
		panel.add(button);
				
		
		// RadioCheck component
		radio = new JCheckBox("Remember Me");
		radio.setBounds(198, 102, 100, 28);
		panel.add(radio);
		
		frame.setVisible(true);
		
	}

	@Override
	public void actionPerformed(ActionEvent e) {

		String Username = username.getText();
		String Password1 = Password.getText();
		
		if(Username.equals("java") && Password1.equals("123")) {
			JOptionPane.showMessageDialog(null, "Login Successful");
		}else {
			JOptionPane.showMessageDialog(null, "Username or Password mismatch ");
		}
	}
}
