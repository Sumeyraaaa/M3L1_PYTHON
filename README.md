# M3L1_PYTHON
from flask import Flask
import random

app = Flask(__name__) 


facts_list = ["Elon Musk, sosyal ağların içeriği görüntülemek için mümkün olduğunca fazla zaman harcamanız için bizi platformun içinde tutmak üzere tasarlandığını iddia ediyor.",
              "2018 yılında yapılan bir araştırmaya göre 18-34 yaş arası kişilerin %50'den fazlası akıllıteelfonlarına bağımlı olduğunu düşünüyor.",
              "Sosyal ağların olumlu ve olumsuz yanları var ve bu platformları kullanırken her ikisinin de farkında olmalıyız.",
              "Teknoloji bağımlılığı çalışması,modern bilimsel araştırmanın en alakalı alanlarından biridir."]

@app.route("/")
def hello_world():
    return f'<a href="/rasgele">Rastgele bir gerçeği görüntüle!</a>'

@app.route("/rastgele")
def rastgele():
    return f'<p>{random.choice(facts_list)}</p>'

liste = ["yazı", "tura"]
@app.route("/yazitura")
def yazitura():
    return f'<p>{random.choice(liste)}</p>'


app.run(debug=True)             
