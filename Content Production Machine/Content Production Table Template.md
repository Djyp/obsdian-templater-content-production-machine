---

database-plugin: basic

---

```yaml:dbfolder
name: <%* tR += tp.file.folder() %>
description: Content Production Machine
columns:
  __file__:
    key: __file__
    id: __file__
    input: markdown
    label: File
    accessorKey: __file__
    isMetadata: true
    skipPersist: false
    isDragDisabled: false
    csvCandidate: true
    position: 1
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: true
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  createdAt:
    input: calendar_time
    accessorKey: createdAt
    key: createdAt
    id: createdAt
    label: createdAt
    position: 2
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  channel:
    input: text
    accessorKey: channel
    key: channel
    id: channel
    label: channel
    position: 5
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  mandatoryPredecessor:
    input: text
    accessorKey: mandatoryPredecessor
    key: mandatoryPredecessor
    id: mandatoryPredecessor
    label: mandatoryPredecessor
    position: 4
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  status:
    input: select
    accessorKey: status
    key: status
    id: status
    label: status
    position: 3
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 113
    options:
      - { label: "Idea", value: "Idea", color: "hsl(10,56%,91%)"}
      - { label: "Maybe", value: "Maybe", color: "hsl(0,59%,88%)"}
      - { label: "NextUp", value: "NextUp", color: "hsl(350,65%,77%)"}
      - { label: "Scheduled", value: "Scheduled", color: "hsl(71, 95%, 90%)"}
      - { label: "Writing", value: "Writing", color: "hsl(115,54%,76%)"}
      - { label: "Production", value: "Production", color: "hsl(170,57%,73%)"}
      - { label: "PostProduction", value: "PostProduction", color: "hsl(189,71%,73%)"}
      - { label: "ReadyToPost", value: "ReadyToPost", color: "hsl(217,92%,76%)"}
      - { label: "Published", value: "Published", color: "hsl(232,97%,85%)"}
      - { label: "OnHold", value: "OnHold", color: "hsl(230,13%,55%)"}
      - { label: "stopped", value: "stopped", color: "hsl(325, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  type:
    input: text
    accessorKey: type
    key: type
    id: type
    label: type
    position: 6
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  topicCategory:
    input: text
    accessorKey: topicCategory
    key: topicCategory
    id: topicCategory
    label: topicCategory
    position: 7
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Notes:
    input: text
    accessorKey: Notes
    key: Notes
    id: Notes
    label: Notes
    position: 8
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  publishedAt:
    input: calendar_time
    accessorKey: publishedAt
    key: publishedAt
    id: publishedAt
    label: publishedAt
    position: 9
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  postedUrls:
    input: text
    accessorKey: postedUrls
    key: postedUrls
    id: postedUrls
    label: postedUrls
    position: 10
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Action_Items:
    input: formula
    accessorKey: Action_Items
    key: Action_Items
    id: Action_Items
    label: Action Items
    position: 11
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      formula_query: "[${row.__tasks__.map(t=>t.text)}]"
  Next_Action_Date:
    input: formula
    accessorKey: Next_Action_Date
    key: Next_Action_Date
    id: Next_Action_Date
    label: Next Action Date
    position: 12
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      formula_query: ${row.__tasks__.filter(t=>!t.completed && t.scheduled).sort((t1,t2)=>t1.scheduled - t2.scheduled)[0].scheduled.toString().slice(0,10)}
  tags:
    input: text
    accessorKey: tags
    key: tags
    id: tags
    label: tags
    position: 13
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
config:
  remove_field_when_delete_column: false
  cell_size: wide
  sticky_first_column: false
  group_folder_column: 
  remove_empty_folders: false
  automatically_group_files: false
  hoist_files_with_empty_attributes: true
  show_metadata_created: false
  show_metadata_modified: false
  show_metadata_tasks: false
  show_metadata_inlinks: false
  show_metadata_outlinks: false
  show_metadata_tags: false
  source_data: query
  source_form_result: "FROM \"<%* const productionsDir = tp.file.folder(true) + "/Productions"
tR += productionsDir %>\""
  source_destination_path: <%* tR += productionsDir %>
  row_templates_folder: Extra/Templates
  current_row_template: Extra/Templates/Content Production Machine/Content Production Template.md
  pagination_size: 50
  font_size: 16
  enable_js_formulas: false
  formula_folder_path: Extra/Views/DBFolder
  inline_default: false
  inline_new_position: last_field
  date_format: yyyy-MM-dd
  datetime_format: "yyyy-MM-dd HH:mm:ss"
  metadata_date_format: "yyyy-MM-dd HH:mm:ss"
  enable_footer: false
  implementation: default
filters:
  enabled: false
  conditions:
```