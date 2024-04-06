# Beep Boop

### Description: Chase stumbled upon Geometry Dash installed on Anthony's laptop, shaking his head and muttering, "This is oh so silly".

This one is pretty simple, beep boop = robots. 

Click the given link and go to robots.txt https://beep-boop.ctf.ritsec.club/robots.txt 

    User-agent: *
    Disallow: /  # Disallow all robots from indexing any content

    UlN7ZzMwbTJ0eV9kQHNoXyFzX2whZjN9

We find a Base64 encoded string UlN7ZzMwbTJ0eV9kQHNoXyFzX2whZjN9 -> Base64 decode 

Flag: RS{g30m2ty_d@sh_!s_l!f3}
