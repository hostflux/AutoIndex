# AutoIndex PHP Script

### Template Variables

**This is a list of all the variables that can be used in the template files.**

### global_header.tpl / global_footer.tpl

Info about the current directory:

| Variable           | Description                                           |
| ------------------ | ----------------------------------------------------- |
| `{info:dir}`       | path of the current directory, including the base dir |
| `{info:subdir}`    | path of the current directory, excluding the base dir |
| `{info:version}`   | version of AutoIndex                                  |
| `{info:page_time}` | time (in milliseconds) to generate the page           |

All words from the language file:

| Variable      | Description                       |
| ------------- | --------------------------------- |
| `{words:foo}` | see language file for all options |

All settings from the config file:

| Variable       | Description           |
| -------------- | --------------------- |
| `{config:foo}` | configuration options |

	See AutoIndex.conf.php for all options

Another specific file can be included using the {include} command:

| Variable             | Description                                                       |
| -------------------- | ----------------------------------------------------------------- |
| `{include:filename}` | anything between `/* */` will not be displayed in the HTML output |

### table_header.tpl / table_footer.tpl

All previously mentioned variables, plus:

Info about current directory:

| Variable                     | Description                        |
| ---------------------------- | ---------------------------------- |
| `{info:path_nav}`            | display navagable path             |
| `{info:total_files}`         | display total files                |
| `{info:total_folders}`       | display total folders              |
| `{info:total_size}`          | display total size                 |
| `{info:total_downloads}`     | display total downloads            |
| `{info:search_box}`          | display search box                 |
| `{info:login_box}`           | display login box                  |
| `{info:archive_link}`        | display archive link               |
| `{info:previous_page_link}`  | display link to the previous page  |
| `{info:next_page_link}`      | display link to the next page      |
| `{info:current_page_number}` | display number of the current page |
| `{info:last_page_number}`    | display number of the last page    |

If-statements:

| Variable                      | Description                                |
| ----------------------------- | ------------------------------------------ |
| `{if:show_dir_size}`          | `show_dir_size` = true / false             |
| `{if:search_enabled}`         | `search_enabled` = true / false            |
| `{if:use_login_system}`       | `use_login_system` = true / false          |
| `{if:must_login_to_download}` | `must_login_to_download` = true / false    |
| `{if:days_new}`               | `days_new` = true / false                  |
| `{if:thumbnail_height}`       | `thumbnail_height` = pixels / false        |
| `{if:icon_path}`              | `icon_path` = icon path / false            |
| `{if:log_file}`               | `log_file` = file name / false [1]         |
| `{if:description_file}`       | `description_file` = file name / false [2] |
| `{if:download_count}`         | `download_count` = file name / false [3]   |
| `{if:entries_per_page}`       | `entries_per_page` = number / false        |

	[1] File name to store visitor traffic
	[2] File name with folder and/or file descriptions
	[3] File name to store downloads
 	
	To end an if-statement, use {end if:varibale}
	For example, {if:days_new} ... {end if:days_new}

	Use AutoIndex.conf.php for variable settings

Sort modes:

| Variable             | Description                 |
| -------------------- | --------------------------- |
| `{sort:filename}`    | sort on file name           |
| `{sort:size}`        | sort on size                |
| `{sort:m_time}`      | sort on time                |
| `{sort:description}` | sort on description         |
| `{sort:downloads}`   | sort on number of downloads |

### each_file.tpl

All previously mentioned variables, plus:

Properties for individual files:

| Variable                               | Description                                                       |
| -------------------------------------- | ----------------------------------------------------------------- |
| `{file:filename}`                      | name of the file or folder                                        |
| `{file:link}`                          | link to the file (using the ?dir and ?file parameters in the URL) |
| `{file:file_ext}`                      | file extension ("dir" for a directory)                            |
| `{file:size}`                          | size (formatted as a string)                                      |
| `{file:bytes}`                         | size (in bytes)                                                   |
| `{file:date}`                          | date modified (formatted as a string)                             |
| `{file:a_time}`                        | date and time accessed                                            |
| `{file:m_time}`                        | date and time modified                                            |
| `{file:num_subfiles}`                  | for a directory, the number of files it contains [1]	             |
| `{file:thumbnail}`                     | for images, it will display a thumbnail                           |
| `{file:md5_link}`                      | link to get the md5sum of the file                                |
| `{file:downloads}`                     | number of times this file has been downloaded                     |
| `{file:description}`                   | description of the current file                                   |
| `{file:icon}`                          | icon image for the filetype                                       |
| `{file:parent_dir}`                    | name of the file's parent directory                               |
| `{file:tr_class}`                      | this returns "light_row" or "dark_row" for every other file       |
| `{file:if:is_file} ... {end if}`       | true if it is a file                                              |
| `{file:if:is_dir} ... {end if}`        | true if it is a folder or link to parent directory                |
| `{file:if:is_real_dir} ... {end if}`   | true if it is a folder                                            |
| `{file:if:is_parent_dir} ... {end if}` | true if it is a link to parent directory                          |
| `{do_every:x} ... {end do_every}`      | where x is a number [2]                                           |

	[1] Use {file:if:is_real_dir}{file:num_subfiles}{end if}
	[2] The code in between will be displayed every x files

---

**[AutoIndex PHP Script](https://github.com/hostflux/AutoIndex)**
