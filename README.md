# frontend
from BeautifulSoup import BeautifulSoup
import urllib2
import re
 
html_page = urllib2.urlopen("https://github.com/rajita5g3/frontend/wiki/_new")
soup = BeautifulSoup(html_page)
for link in soup.findAll('a', attrs={'href': re.compile("^http://")}):
    print link.get('href')
