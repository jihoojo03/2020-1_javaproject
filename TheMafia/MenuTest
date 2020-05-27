package TheMafia;
import javax.swing.*;

public class MenuTest extends JFrame {

	MenuTest(){
		setTitle("Menu 제작");
		createMenu(); // Create menu
		setSize(250, 200);
		setVisible(true);
	}
	
	void createMenu() {
		JMenuBar mb = new JMenuBar();
		JMenu screenMenu = new JMenu("스토리");
		
		screenMenu.add(new JMenuItem("진행상황"));
		screenMenu.add(new JMenuItem("분기점 선택"));
		screenMenu.add(new JMenuItem("등장인물"));
		screenMenu.addSeparator();
		screenMenu.add(new JMenuItem("Exit"));
		
		mb.add(screenMenu);
		mb.add(new JMenu("편집"));
		mb.add(new JMenu("실행"));
		mb.add(new JMenu("도움말"));
		setJMenuBar(mb);
	}


}
