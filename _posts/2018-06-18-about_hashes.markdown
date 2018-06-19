---
layout: post
title:      "About Hashes"
date:       2018-06-19 01:35:35 +0000
permalink:  about_hashes
---


Hashes are an inevitable part of coding and though the concept of hashes is simple, its syntax  can be confusing, for me at least.  So I'm trying to write about it to further ingrain it to my knowledge. For those who read this post, I hope this will help in cementing your knowledge about hashes.

So, hashes can be written in the following ways when passing it as an argument to a method

```
#1
(hash_name[:key]) or (hash_name["key"])

#2
(key1: value, key2: value)

#3
(args = {key1: value, key2: value}) #this example was actually part of a lab

#4
(hasname) #the whole hash is put in the argument
```

Implementation examples of the above arguments are as follows (Emphasis on the syntax and not on the logic of the code) :

```
#1
def initialize(hash_name[:name])
   @name = movie[:name]
end
 
 
 #2 
 def update_title
     new_moviename = Movie.find_by(movie_name: "The Matrix")
	end
 

 
 #3 from activerecord-crud lab
 def can_be_created_in_a_block(args = { title: "Home Alone", release_date: 1990 })
  Movie.create do |m|
    m.title = args[:title]
    m.release_date = args[:release_date]
    m.save
  end
end

#4 from Sinatra Neste Forms Lab
def initialize(params)
    @name = params[:name]
    @grade = params[:grade]
    STUDENTS << self
  end
 
```

When using the hash name and key (Example #1), the pattern I'm seeing is to write it this way (Note placement of colon, colon is before the key):

```
hash_name[:key]
```

When using the key-value pair method  (Example #2,#3) the pattern is below (Colon is after the key):

```
key: value
```

I'll be adding on this as I get to more complicated examples but this will do for now. Hope this is helpful for the readers :)
