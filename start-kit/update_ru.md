### file: settings/config/config.php
находим:

`return $config;`

перед ней добавляем:

`$config['head']['default']['css'][] = '___path.skin.dir___/assets/css/compatibility.css';`

### file: tpls/topics/topic.type_default-edit.tpl
находим:

`{include file='commons/common.editor.tpl'}`

заменяем на:

`{include file='commons/common.editor.tpl' sTargetType='topic'}`

находим:

`<input type="hidden" name="security_key" value="{$ALTO_SECURITY_KEY}"/>`

после нее добавляем:

`<input type="hidden" id="topic_id"  name="topic_id" value="{$_aRequest.topic_id}"/>`

### file: tpls/editors/editor.markitup.tpl

находим:

`ls.lang.load({lang_load name="panel_title_h4,panel_title_h5,panel_title_h6,panel_b,panel_i,panel_u,panel_s,panel_url,panel_url_promt,panel_code,panel_video,panel_image,panel_cut,panel_quote,panel_list,panel_list_ul,panel_list_ol,panel_title,panel_clear_tags,panel_video_promt,panel_list_li,panel_image_promt,panel_user,panel_user_promt"});`

заменяем на:

`ls.lang.load({lang_load name="panel_photoset,panel_spoiler,panel_title_h4,panel_title_h5,panel_title_h6,panel_b,panel_i,panel_u,panel_s,panel_url,panel_url_promt,panel_code,panel_video,panel_image,panel_cut,panel_quote,panel_list,panel_list_ul,panel_list_ol,panel_title,panel_clear_tags,panel_video_promt,panel_list_li,panel_image_promt,panel_user,panel_user_promt"});`

### file: tpls/editors/editor.tinymce.tpl

находим:

`ls.lang.load({lang_load name="panel_title_h4,panel_title_h5,panel_title_h6"});`

заменяем на:

`ls.lang.load({lang_load name="panel_photoset,panel_spoiler,panel_title_h4,panel_title_h5,panel_title_h6"});`
