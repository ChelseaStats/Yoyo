# Yoyo
Yo notifications when Chelsea do a goal. no cake.


    <?php
    	print 'hello <br/>';
    	
        require_once('yo.class.php');
        $token = 'xxxxx';
    
        try {
            $yo = new \cfc\Yo($token);
            // send a yo to all subscribers
            $yo->sendAll('https://m.thechels.uk'); // or you can yo without link: $yo->sendAll();
            // send a yo to one subscriber
            $yo->sendUser('CHELSEASTATS', 'https://m.thechels.uk'); 
            // or you can yo without link: $yo->sendUser('CHELSEASTATS');
            // count of subscribers
            $count = $yo->subscribersCount();
            echo 'Count: ' . $count;
        } catch (\cfc\YoException $e) {
            echo "<br/>:: Error #" . $e->getCode() . ": " . $e->getMessage();
        }
    
    	print 'Goodbye <br/>';
