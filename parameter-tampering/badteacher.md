# Bad Teacher 

## Description
This is a simple web application that allows teachers to view their students' profiles. The teacher can log in with the provided password and view the students' names. The teacher can then click on the student's name to view their profile.

## Step to reproduce 
1. Go to the login page with the provided password
> username: `s12345`
> password: `password`

2. When you log in, you will see the 3 students' names
3. Right click on any of the student's name and click on inspect
4. You will see the student's name in the HTML code
5. Edit this part
```html
<select class="form-control" name="username"> <option value="p5678902">Nicholas Lim</option> <option value="p5678903">Susan Leah Michael</option> <option value="p5678904">Timothy Chang</option> </select>
```

to this
```html
<select class="form-control" name="username"> <option value="p5678901">Nicholas Lim</option> <option value="p5678903">Susan Leah Michael</option> <option value="p5678904">Timothy Chang</option> <option value="p5678901"> Nicole Fong </option> </select>
```

6. Click on view profile, this will show you the student's profile of Nicole Fang

