packages:

- poetry add fastapi
- poetry add uvicorn
- poetry add python-jose[cryptography]
- poetry add passlib[bcrypt]
- poetry add sqlalchemy 
- poetry add alembic
- poetry add python-multipart
- poetry add pydantic[email]  
- poetry add jinja2 
- poetry add psycopg2  
- poetry add libgravatar

[//]: # (- pip install pydantic[email]   )
[//]: # (- pip install jinja2        )


- poetry add fastapi uvicorn pydantic[email] jinja2 python-jose[cryptography] passlib[bcrypt] sqlalchemy alembic psycopg2 python-multipart libgravatar


commands: 
- alembic init migrations
- alembic revision --autogenerate -m "initial"
- alembic upgrade head
- uvicorn main:app --host localhost --port 8000 --reload

- поміняти в env: 

[//]: # (from logging.config import fileConfig)

[//]: # ()
[//]: # (from sqlalchemy import engine_from_config)

[//]: # (from sqlalchemy import pool)

[//]: # ()
[//]: # (from alembic import context)

[//]: # ()
[//]: # (from src.database.db import URI)

[//]: # (from src.database.models import Base)

[//]: # ()
[//]: # (# this is the Alembic Config object, which provides)

[//]: # (# access to the values within the .ini file in use.)

[//]: # (config = context.config)

[//]: # ()
[//]: # (# Interpret the config file for Python logging.)

[//]: # (# This line sets up loggers basically.)

[//]: # (if config.config_file_name is not None:)

[//]: # (    fileConfig&#40;config.config_file_name&#41;)

[//]: # ()
[//]: # (# add your model's MetaData object here)

[//]: # (# for 'autogenerate' support)

[//]: # (# from myapp import mymodel)

[//]: # (# target_metadata = mymodel.Base.metadata)

[//]: # (target_metadata = Base.metadata)

[//]: # ()
[//]: # (# other values from the config, defined by the needs of env.py,)

[//]: # (# can be acquired:)

[//]: # (# my_important_option = config.get_main_option&#40;"my_important_option"&#41;)

[//]: # (# ... etc.)

[//]: # (config.set_main_option&#40;"sqlalchemy.url", URI&#41;)

- ...