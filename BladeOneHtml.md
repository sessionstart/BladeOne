#BladeOneHtml extension library (optional)

Requires: BladeOne

For using this tag, the code requires to use the class BladeOneHtml

##New Tags

### Select/endselect

```html
@select('id1')
    @item('0','--Select a country--',$countrySelected,'')
    @items($countries,'id','name',$countrySelected,'')
@endselect()
```

- @select/@endselect creates the **select** tag. The first value is the id and name of the tag.
- @item allows to add one element **option** tag. 
-   The first value is the id and the second is the visible text. 
-   The third tag indicates the selected element. It could be a single value or an array of elements.
- @items allows to add one list of elements **option** tag. 
-   The first value is the list of values, 
-   the second and third is the id and name. 
-   And the fourth one is the selected value (optional)
    
![select](http://i.imgur.com/yaMavQB.jpg?1)

### Input

```html
@input('iduser',$currentUser,'text'[,$extra])
```

@input creates a **input** tag. The first value is the id/name, the second is the default value, the third is the type (by default is text for textbox)*[]: 

### Form/endform
```form
@form(['action'],['post'][,$extra])
    ... form goes here
@endform
```
@form creates **form** html tag. The first value (optional) is the action, the second value (optional) is the method ('post','get')

###listboxes
```html
@listboxes('idlistbox',$countries,'id','name',$multipleSelect)
```

- @listboxes(id,$listvalues,$fieldid,$fieldvalue,·selected,[$extra]) Creates a list box
-   The id (indicates the id of the object. It shoulds be unique. I
-   $listvalues indicates the vlaues to show in the object.
-   $fieldid indicates the field used as key.
-   $fieldvalue indicates the field used to show.
-   $selected indicates the selected values.
-   $extra (optional) indicates the extra value (see note below).

###selectgroup

###radio/endradio

###checkbox/endcheckbox

###item/trio

###items/trios

###textarea

###hidden

###label

###commandbutton



### NOTE: Extra Parameter
 
Additionally, you can add an (optional) last parameter with additional value (see the example of @select)

```html
 <!-- code using bootstrap -->
 <div class="form-group">
  <label for="sel1">Select list:</label>
        @select('id1')
            @item('0','--Select a country--',"",class='form-control'")
            @items($countries,'id','name',"",$countrySelected)
        @endselect()
  </select>
</div>
```

