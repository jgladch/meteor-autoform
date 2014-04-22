## Public and Private API ##

_API documentation automatically generated by [docmeteor](https://github.com/raix/docmeteor)._

***

__File: ["utility.js"](utility.js) Where: {client}__

***

### <a name="Utility.cleanNulls"></a>*utility*.cleanNulls(doc)&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*
*This method __cleanNulls__ is defined in `Utility`*

__Arguments__

* __doc__ *{Object}*  

 Source object


__Returns__  *{Object}*


Returns an object in which all properties with null, undefined, or empty
string values have been removed, recursively.

> ```cleanNulls: function cleanNulls(doc, isArray) { ...``` [utility.js:11](utility.js#L11)


-

### <a name="Utility.reportNulls"></a>*utility*.reportNulls(flatDoc)&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*
*This method __reportNulls__ is defined in `Utility`*

__Arguments__

* __flatDoc__ *{Object}*  

 An object with no properties that are also objects.


__Returns__  *{Object}*
An object in which the keys represent the keys in the

original object that were null, undefined, or empty strings, and the value
of each key is "".

> ```reportNulls: function reportNulls(flatDoc) { ...``` [utility.js:38](utility.js#L38)


-

### <a name="Utility.docToModifier"></a>*utility*.docToModifier(doc)&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*
*This method __docToModifier__ is defined in `Utility`*

__Arguments__

* __doc__ *{Object}*  

 An object to be converted into a MongoDB modifier


__Returns__  *{Object}*
A MongoDB modifier.


Converts an object into a modifier by flattening it, putting keys with
null, undefined, and empty string values into `modifier.$unset`, and
putting the rest of the keys into `modifier.$set`.

> ```docToModifier: function docToModifier(doc) { ...``` [utility.js:57](utility.js#L57)


-

### <a name="Utility.getSelectValues"></a>*utility*.getSelectValues(select)&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*
*This method __getSelectValues__ is defined in `Utility`*

__Arguments__

* __select__ *{[Element](#Element)}*  

 DOM Element from which to get current values


__Returns__  *{string[]}*


Gets a string array of all the selected values in a given `select` DOM element.

> ```getSelectValues: function getSelectValues(select) { ...``` [utility.js:84](utility.js#L84)


-

### <a name="Utility.maybeNum"></a>*utility*.maybeNum(val)&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*
*This method __maybeNum__ is defined in `Utility`*

__Arguments__

* __val__ *{string}*  

__Returns__  *{String|Number}*


If the given string can be converted to a number, returns the number.
Otherwise returns the string.

> ```maybeNum: function maybeNum(val) { ...``` [utility.js:107](utility.js#L107)


-

### <a name="Utility.lookup"></a>*utility*.lookup(obj)&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*
*This method __lookup__ is defined in `Utility`*

__Arguments__

* __obj__ *{Any}*  

__Returns__  *{Any}*


If `obj` is a string, returns the value of the property with that
name on the `window` object. Otherwise returns `obj`.

> ```lookup: function lookup(obj) { ...``` [utility.js:125](utility.js#L125)


-

### <a name="Utility.getDefs"></a>*utility*.getDefs(ss, name)&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*
*This method __getDefs__ is defined in `Utility`*

__Arguments__

* __ss__ *{[SimpleSchema](#SimpleSchema)}*  
* __name__ *{String}*  

__Returns__  *{Object}*
Schema definitions object


Returns the schema definitions object from a SimpleSchema instance. Equivalent to calling
`ss.schema(name)` but handles throwing errors if `name` is not a string or is not a valid
field name for this SimpleSchema instance.

> ```getDefs: function getDefs(ss, name) { ...``` [utility.js:145](utility.js#L145)


-

### <a name="Utility.objAffectsKey"></a>*utility*.objAffectsKey({Object}, {String})&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*
*This method __objAffectsKey__ is defined in `Utility`*

__Arguments__

* __{Object}__ *{any}*  

 obj

* __{String}__ *{any}*  

 key


__Returns__  *{Boolean}*

__TODO__
```
* should make this a static method in MongoObject
```


> ```objAffectsKey: function objAffectsKey(obj, key) { ...``` [utility.js:163](utility.js#L163)


-

### <a name="Utility.expandObj"></a>*utility*.expandObj({Object})&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*
*This method __expandObj__ is defined in `Utility`*

__Arguments__

* __{Object}__ *{any}*  

 doc


__Returns__  *{Object}*


Takes a flat object and returns an expanded version of it.

> ```expandObj: function expandObj(doc) { ...``` [utility.js:175](utility.js#L175)


-

### <a name="Utility.compactArrays"></a>*utility*.compactArrays({Object})&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*
*This method __compactArrays__ is defined in `Utility`*

__Arguments__

* __{Object}__ *{any}*  

 obj


__Returns__  *{undefined}*


Edits the object by reference, compacting any arrays at any level recursively.

> ```compactArrays: function compactArrays(obj) { ...``` [utility.js:212](utility.js#L212)


-

### <a name="Utility.getSimpleSchemaFromContext"></a>*utility*.getSimpleSchemaFromContext({Object})&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*
*This method __getSimpleSchemaFromContext__ is defined in `Utility`*

__Arguments__

* __{Object}__ *{any}*  

 context


__Returns__  *{SimpleSchema}*


Given a context object that may or may not have schema and collection properties,
returns a SimpleSchema instance or throws an error if one cannot be obtained.

> ```getSimpleSchemaFromContext: function getSimpleSchemaFromContext(context, formId) { ...``` [utility.js:234](utility.js#L234)


-

### <a name="Utility.isValidDateString"></a>*utility*.isValidDateString({String})&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*
*This method __isValidDateString__ is defined in `Utility`*

__Arguments__

* __{String}__ *{any}*  

 dateString


__Returns__  *{Boolean}*


Returns `true` if dateString is a "valid date string"

> ```isValidDateString: function isValidDateString(dateString) { ...``` [utility.js:268](utility.js#L268)


-

### <a name="Utility.isValidTimeString"></a>*utility*.isValidTimeString({String})&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*
*This method __isValidTimeString__ is defined in `Utility`*

__Arguments__

* __{String}__ *{any}*  

 timeString


__Returns__  *{Boolean}*


Returns `true` if timeString is a "valid time string"

> ```isValidTimeString: function isValidTimeString(timeString) { ...``` [utility.js:280](utility.js#L280)


-

### <a name=""></a>({Date})&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*

__Arguments__

* __{Date}__ *{any}*  

 date


__Returns__  *{String}*


Returns a "valid date string" representing the local date.

> ```dateToDateString: function dateToDateString(date) { ...``` [utility.js:297](utility.js#L297)


-

### <a name=""></a>({Date})&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*

__Arguments__

* __{Date}__ *{any}*  

 date


__Returns__  *{String}*


Returns a "valid date string" representing the date converted to the UTC time zone.

> ```dateToDateStringUTC: function dateToDateStringUTC(date) { ...``` [utility.js:316](utility.js#L316)


-

### <a name=""></a>({Date})&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*

__Arguments__

* __{Date}__ *{any}*  

 date


__Returns__  *{String}*


Returns a "valid normalized forced-UTC global date and time string" representing the time
converted to the UTC time zone and expressed as the shortest possible string for the given
time (e.g. omitting the seconds component entirely if the given time is zero seconds past the minute).

http:
http:

> ```dateToNormalizedForcedUtcGlobalDateAndTimeString: function dateToNormalizedForcedUtcGlobalDateAndTimeString(date) { ...``` [utility.js:340](utility.js#L340)


-

### <a name=""></a>({String})&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*

__Arguments__

* __{String}__ *{any}*  

 dateString


__Returns__  *{Boolean}*


Returns true if dateString is a "valid normalized forced-UTC global date and time string"

> ```isValidNormalizedForcedUtcGlobalDateAndTimeString: function isValidNormalizedForcedUtcGlobalDateAndTimeString(dateString) { ...``` [utility.js:351](utility.js#L351)


-

### <a name="Utility.dateToNormalizedLocalDateAndTimeString"></a>*utility*.dateToNormalizedLocalDateAndTimeString(date, offset)&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*
*This method __dateToNormalizedLocalDateAndTimeString__ is defined in `Utility`*

__Arguments__

* __date__ *{[Date](#Date)}*  
* __offset__ *{String}*  

 A valid offset string (to pass to moment.zone)


__Returns__  *{String}*


Returns a "valid normalized local date and time string".

> ```dateToNormalizedLocalDateAndTimeString: function dateToNormalizedLocalDateAndTimeString(date, offset) { ...``` [utility.js:370](utility.js#L370)


-

### <a name=""></a>({String})&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*

__Arguments__

* __{String}__ *{any}*  

 dtString


__Returns__  *{Boolean}*


Returns true if dtString is a "valid normalized local date and time string"

> ```isValidNormalizedLocalDateAndTimeString: function isValidNormalizedLocalDateAndTimeString(dtString) { ...``` [utility.js:383](utility.js#L383)


-

### <a name="Utility.normalizeContext"></a>*utility*.normalizeContext({Object}, name)&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*
*This method __normalizeContext__ is defined in `Utility`*

__Arguments__

* __{Object}__ *{any}*  

 context A context object, potentially with an `atts` or `autoform` property.

* __name__ *{String}*  

 The name of the helper or component we're calling from, for in a potential error message.


__Returns__  *{Object}*
Normalized context object


Returns an object with `afc`, `af`, and `atts` properties, normalized from whatever object is passed in.
This helps deal with the fact that we have to pass the ancestor autoform's context to different
helpers and components in different ways, but in all cases we want to get access to it and throw
an error if we can't find an autoform context.

> ```normalizeContext: function autoFormNormalizeContext(context, name) { ...``` [utility.js:404](utility.js#L404)


***

__File: ["form-preserve.js"](form-preserve.js) Where: {client}__

***

### <a name="FormPreserve"></a>new FormPreserve(migrationName)&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method is private*

__Arguments__

* __migrationName__ *{String}*  


Internal helper object to preserve form inputs across Hot Code Push
and across "pages" navigation if the option is enabled.

> ```FormPreserve = function formPreserveConstructor(migrationName) { ...``` [form-preserve.js:9](form-preserve.js#L9)


***

__File: ["autoform.js"](autoform.js) Where: {client}__

***

### <a name="AutoForm.addHooks"></a>*autoform*.addHooks(formIds, hooks)&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method __addHooks__ is defined in `AutoForm`*

__Arguments__

* __formIds__ *{[String[]](#String[])|String|null}*  

 Form `id` or array of form IDs to which these hooks apply. Specify `null` to add hooks that will run for every form.

* __hooks__ *{Object}*  

 Hooks to add, where supported names are "before", "after", "formToDoc", "docToForm", "onSubmit", "onSuccess", and "onError".


__Returns__  *{undefined}*


Defines hooks to be used by one or more forms. Extends hooks lists if called multiple times for the same
form.

> ```AutoForm.addHooks = function autoFormAddHooks(formIds, hooks, replace) { ...``` [autoform.js:20](autoform.js#L20)


-

### <a name="AutoForm.hooks"></a>*autoform*.hooks(hooks)&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method __hooks__ is defined in `AutoForm`*

__Arguments__

* __hooks__ *{Object}*  

__Returns__  *{undefined}*


Defines hooks by form id. Extends hooks lists if called multiple times for the same
form.

> ```AutoForm.hooks = function autoFormHooks(hooks, replace) { ...``` [autoform.js:56](autoform.js#L56)


-

### <a name="AutoForm.resetForm"></a>*autoform*.resetForm(formId)&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method __resetForm__ is defined in `AutoForm`*

__Arguments__

* __formId__ *{String}*  

__Returns__  *{undefined}*


Resets validation for an autoform.

> ```AutoForm.resetForm = function autoFormResetForm(formId) { ...``` [autoform.js:70](autoform.js#L70)


-

### <a name="AutoForm.setDefaultTemplateForType"></a>*autoform*.setDefaultTemplateForType(type, template)&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method __setDefaultTemplateForType__ is defined in `AutoForm`*

__Arguments__

* __type__ *{String}*  
* __template__ *{String}*  


> ```AutoForm.setDefaultTemplateForType = function autoFormSetDefaultTemplateForType(type, template) { ...``` [autoform.js:138](autoform.js#L138)


-

### <a name="AutoForm.getDefaultTemplateForType"></a>*autoform*.getDefaultTemplateForType(type)&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method __getDefaultTemplateForType__ is defined in `AutoForm`*

__Arguments__

* __type__ *{String}*  

__Returns__  *{String}*
Template name


Reactive.

> ```AutoForm.getDefaultTemplateForType = function autoFormGetDefaultTemplateForType(type) { ...``` [autoform.js:157](autoform.js#L157)


-

### <a name="AutoForm.getFormValues"></a>*autoform*.getFormValues(formId)&nbsp;&nbsp;<sub><i>Client</i></sub> ###

*This method __getFormValues__ is defined in `AutoForm`*

__Arguments__

* __formId__ *{String}*  

 The `id` attribute of the `autoForm` you want current values for.


__Returns__  *{Object}*


Returns an object representing the current values of all schema-based fields in the form.
The returned object contains two properties, "insertDoc" and "updateDoc", which represent
the field values as a normal object and as a MongoDB modifier, respectively.

> ```AutoForm.getFormValues = function (formId) { ...``` [autoform.js:175](autoform.js#L175)



-
Returns schema keys that are direct children of the given schema key
XXX this could be a method on ss