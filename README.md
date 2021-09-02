<?php

# snippet-notification-attach-pdf

add_filter( 'gform_notification', 'change_user_notification_attachments', 10, 3 );
function change_user_notification_attachments( $notification, $form, $entry ) {

    if ( $notification['name'] == 'User Notification' ) {
        $url = 'http://yoursite.com/path/to/file.pdf';
        $notification['attachments'][] = $url;
    }

    return $notification;
}
