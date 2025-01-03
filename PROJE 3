import sys
from PyQt6.QtWidgets import *
import ticari

class LoginWindow(QMainWindow):
    def __init__(self):
        super().__init__()
        self.setWindowTitle("Login Ekranı")
        central_widget = QWidget()
        layout = QVBoxLayout()

        label_username = QLabel("Kullanıcı Adı:")
        self.username_input = QLineEdit()
        layout.addWidget(label_username)
        layout.addWidget(self.username_input)

        label_password = QLabel("Şifre:")
        self.password_input = QLineEdit()
        self.password_input.setEchoMode(QLineEdit.EchoMode.Password)
        layout.addWidget(label_password)
        layout.addWidget(self.password_input)

        login_button = QPushButton("Giriş Yap")
        login_button.clicked.connect(self.login)
        layout.addWidget(login_button)

        central_widget.setLayout(layout)
        self.setCentralWidget(central_widget)

    def login(self):
        username = self.username_input.text()
        password = self.password_input.text()

        # Kullanıcı adı ve şifreyi kontrol etme - Örnek amaçlı basit bir kontrol
        if username == "admin" and password == "1234":
            self.open_ticari_window()

        else: QMessageBox.warning(self, "Hata", "Geçersiz kullanıcı adı veya şifre!")

    def open_ticari_window(self):
        QMessageBox.information(self, "Başarılı", "Giriş başarılı!\nANA PROGRAMDASINIZ.")
        self.close()  # Login penceresini kapat
        self.ticari_window = ticari.TicariWindow()
        self.ticari_window.show()

def main():
    app = QApplication(sys.argv)
    window = LoginWindow()
    window.show()
    sys.exit(app.exec())

if __name__ == "__main__":
    main()

import sys
from PyQt6.QtWidgets import *

class TicariWindow(QMainWindow):
    def __init__(self):
        super().__init__()

        self.setWindowTitle("Inch çevirici")
        self.arayuz()

    def arayuz(self):
        central_widget = QWidget()
        layout = QVBoxLayout()

        label_cmdeger = QLabel("Cm değeri girin:")
        self.cmdeger_input = QLineEdit()
        layout.addWidget(label_cmdeger)
        layout.addWidget(self.cmdeger_input)

        cevir_button = QPushButton("Çevir")
        cevir_button.clicked.connect(self.mesaj)
        layout.addWidget(cevir_button)

        label_inch = QLabel("Inch değeri:")
        self.inch_input = QLineEdit()
        layout.addWidget(label_inch)
        layout.addWidget(self.inch_input)

        central_widget.setLayout(layout)
        self.setCentralWidget(central_widget)

    def mesaj(self):
        cmdeger = int(self.cmdeger_input.text()) * 2
        self.inch_input.setText(str(cmdeger))
       
def main():
    app = QApplication(sys.argv)
    window = TicariWindow()
    QMessageBox.information(window, "Cm-Inch Çevirici", "Inch çevirici uygulamasına hoş geldiniz.")
    window.show()
    sys.exit(app.exec())

if __name__ == "__main__":
    main()
