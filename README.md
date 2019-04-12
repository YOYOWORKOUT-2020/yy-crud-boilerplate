CRUD OPERATIONS
=========================================================================



A - ROUTES
-------------------------------------------------------------------------


###### GUI ROUTES

```

    /xxx/                       =>  HOME    or redirect : LIST
    /xxx/list                   =>  LIST
    /xxx/find                   =>  FIND
    
    /xxx/new                    =>  CREATE
    /xxx/{pk}                   =>  SHOW    by PK
    /xxx/slug/{slug}            =>  SHOW    by SLUG
    /xxx/{pk}/edit              =>  EDIT    
    /xxx/{pk}/destroy           =>  DESTROY  CONFIRM     
    
    /xxx/list.{ext}             =>  EXPORT LIST by EXTENSION
    /xxx/print                  =>  EXPORT LIST for PRINTING
    /xxx/{pk}.{ext}             =>  EXPORT RECORD by EXTENSION
    /xxx/{pk}/print             =>  EXPORT RECORD for PRINTING
    
    /xxx/{pk}/yyy/              =>  LIST OF Y HAVING X PARENT
    
```


###### ACTIONS AND HTTP VERBS

- home:          GET
- list:          GET
- find:          GET
    - select     POST
- show:          GET
- edit:          GET + POST
    - update:    POST
- create:        GET + POST
    - insert:    POST
- destroy:       GET + POST
    - delete:    POST



B - GUI AND ACTIONS LINKS
-------------------------------------------------------------------------

### HOME
 - show list
 - add new
 - find
 
 
### LIST
  - add new
  - -
  - find
  - export + format
  - print
  
  
### CREATE
 - show list
 - cancel | save
 - -
 - save and continue editing
 - save and create new
 
 
### EDIT
 - show list
 - cancel | save 
 - delete
  
  
### SHOW
 - show list
 - delete
 - -
 - export
 - print
 
 
### DELETE
 - cancel | confirm 
 - -
 - send to trash
   
    


c - RECORDS MIXINS
-------------------------------------------------------------------------

- **draftable** : autosave changes when new or edit
- **trashable** : do not delete , put in trashcan
