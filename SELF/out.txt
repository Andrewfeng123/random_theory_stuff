#include <iostream>
#include <string>
using namespace std;
string wrap(string str){string strr;for(char &c:str){char b[2]={92,0},d[2]={34,0},cc[2]={c,0},e[3]={92,110,0};if(c==b[0]){strr.append(b);strr.append(b);}else if(c==10){strr.append(e);}else if(c==d[0]){strr.append(b);strr.append(d);}else strr.append(cc);}return strr;}
int main() {
string source;
source = "\nsource = \"#include <iostream>\\n#include <string>\\nusing namespace std;\\nstring wrap(string str){string strr;for(char &c:str){char b[2]={92,0},d[2]={34,0},cc[2]={c,0},e[3]={92,110,0};if(c==b[0]){strr.append(b);strr.append(b);}else if(c==10){strr.append(e);}else if(c==d[0]){strr.append(b);strr.append(d);}else strr.append(cc);}return strr;}\\nint main() {\\nstring source;\\nsource = \\\"\" + wrap(source) + \"\\\";\" + source;\ncout << source;\nreturn 0;\n}";
source = "#include <iostream>\n#include <string>\nusing namespace std;\nstring wrap(string str){string strr;for(char &c:str){char b[2]={92,0},d[2]={34,0},cc[2]={c,0},e[3]={92,110,0};if(c==b[0]){strr.append(b);strr.append(b);}else if(c==10){strr.append(e);}else if(c==d[0]){strr.append(b);strr.append(d);}else strr.append(cc);}return strr;}\nint main() {\nstring source;\nsource = \"" + wrap(source) + "\";" + source;
cout << source;
return 0;
}