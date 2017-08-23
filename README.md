
<?php
      $data  = mysqli_connect('localhost', 'root', '', 'hnginterns');
       if (! $data) {die('Error Connecting to Database');}
        $info = mysqli_query($data, "select * from interns");     
    if ($info) {echo '<table><tr><th>S/N</th><th>Name</th><th>Slack Username</th</tr>';
        while ($row = mysqli_fetch_assoc($info)) {
            echo '<tr><td>' . $row['id'] . '</td>'; 
            echo '<td>' . $row['name'] . '</td>'; 
            echo '<td>' . $row['slackname'] . '</td></tr>';}
        echo '</table>';
    }
    ?>
