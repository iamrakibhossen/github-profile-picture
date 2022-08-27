# github-profile-picture
Extract github profile picture via python


# Get github user profile image with BeautifulSoup
```
from bs4 import BeautifulSoup as bs
import requests

github_user = input("Enter your github username: ")

url = "https://github.com/" + github_user

r = requests.get( url )

soup = bs( r.content, "html.parser")

image_url = soup.find("img", {"alt" : "Avatar"})['src']

print( image_url )
```
