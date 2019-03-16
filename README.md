### sandman
---
https://github.com/jeffknupp/sandman

```py
from sandman import app

app.config['SQLACHMY_DATABASE_URI'] = 'sqlite:///chinook'

from sandman.model import activate

activate()

app.run()

from sandman.model import register, Model

class Artist(Model):
  __tablename__ = 'Album'

class Album(Model):
  __tablename__ = 'Album'

class Playlist(Model):
  __tablename__ = 'Playlist'


class Style(Model):
  """ 
  """

  __tablename__ = 'Genre'
  __endpoint__ = 'styles'
  __methods__ = ('GET', 'DELETE')
  __top_level_json_name__ = 'Genres'
  
  @staticmethod
  def validate_GET(resource=None):
    """
    """
    
    if isinstance(resource, list):
      """
      """
      
      if isinstance(resource, list):
        return True
      elif resource and resource.GenreId == 1:
        return False
      return True






```

```sh
sandmanctl sqlite:////tmp/my_database.db

python runserver.py &
curl GET "http://localhost:5000/artists?Name=AC/DC"
```

```
```


