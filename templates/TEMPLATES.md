# AutoIndex PHP Script

## Template Variables

This is a list of all the variables that can be used in the template files.

### global\_header.tpl / global\_footer.tpl

Info about the current directory:

	{info:dir}		the path of the current directory, including the base dir
	{info:subdir}		the path of the current directory, not including the base dir
	{info:version}		the version of AutoIndex
	{info:page\_time}	the time (in milliseconds) it took to generate the page

All words from the language file:

	{words:foo}
	... see language file for all options

All settings from the config file:

	{config:foo}
	... see AutoIndex.conf.php for all options

You can include another specific file using the {include} command:

	{include:filename}

Anything between `/* */` will not be displayed in the HTML output.

### table\_header.tpl / table\_footer.tpl

All previously mentioned variables, plus:

Info about current directory:

	{info:path\_nav}
	{info:total\_files}
	{info:total\_folders}
	{info:total\_size}
	{info:total\_downloads}
	{info:search\_box}
	{info:login\_box}
	{info:archive\_link}
	{info:previous\_page\_link}
	{info:next\_page\_link}
	{info:current\_page\_number}
	{info:last\_page\_number}

If-statements:

	{if:show\_dir\_size}
	{if:search\_enabled}
	{if:use\_login\_system}
	{if:must\_login\_to\_download}
	{if:days\_new}
	{if:thumbnail\_height}
	{if:log\_file}
	{if:description\_file}
	{if:download\_count}
	{if:entries\_per\_page}

To end an if-statement, use `{end if:varibale}`  
For example, `{if:days_new} ... {end if:days_new}`

Sort modes:

	{sort:filename}
	{sort:size}
	{sort:m\_time}
	{sort:description}
	{sort:downloads}

### each\_file.tpl

All previously mentioned variables, plus:

Properties for individual files:

	{file:filename}				the name of the file or folder
	{file:link}				the link to the file (using the ?dir and ?file parameters in the URL)
	{file:file\_ext}			the file extension ("dir" for a directory)
	{file:size}				the size (formatted as a string)
	{file:bytes}				the size (in bytes)
	{file:date}				the date modified (formatted as a string)
	{file:a\_time}				date and time accessed
	{file:m\_time}				date and time modified
	{file:num\_subfiles}			for a directory, the number of files it contains
		Use {file:if:is\_real\_dir}{file:num\_subfiles}{end if}
	{file:thumbnail}			for images, it will display a thumbnail
	{file:md5\_link}			a link to get the md5sum of the file
	{file:downloads}			the number of times this file has been downloaded
	{file:description}			the description of the current file
	{file:icon}				the icon image for the filetype
	{file:parent\_dir}			the name of the file's parent directory
	{file:tr\_class}			this returns "light\_row" or "dark\_row" for every other file
	{file:if:is\_file} ... {end if}		true if it is a file
	{file:if:is\_dir} ... {end if}		true if it is a folder or link to parent directory
	{file:if:is\_real\_dir} ... {end if}	true if it is a folder
	{file:if:is\_parent\_dir} ... {end if}	true if it is a link to parent directory
	{do\_every:x} ... {end do\_every} where x is a number
		The code in between will be displayed every x files

**[AutoIndex PHP Script](https://github.com/hostflux/AutoIndex)**
