# desktop_app
python desktop applications


with open('123.txt', 'r') as f:
    f_contents = f.readlines()
    cal = (f_contents[0:8])
    rez = []
    conditional = 'module=ok'
    for sub in cal:
        rez.append(sub.replace("\n", ""))
    
    print("New List : " + str(rez))    
    calx = rez[0]   
    if calx == conditional:
        print("Healthy")
    elif calx != conditional:
        print("UnHealthy")
    else: 
        print("unknown")

data = ["Health", "DOwn" , "Health","Health"]
data2 = ["Health", "DOwn" , "Health","Health"]

f = open('E:/123.htm', 'a')


def data_to_html_table(data,data2):
        html = '<table border = "2" ><tbody><th>value</th><th>value</th><th>value</th><th>value</th><tr>'
        for items in data,data2:
            for item in items:
                html += '<td>' + str(item) + '</td>'
            html += '</tr><tr>'
        html += '</tr></tbody></table>'
        return html

a = data_to_html_table(data,data2)

f.write(a)
