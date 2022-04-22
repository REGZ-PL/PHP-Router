<?PHP
	CLASS ROUTER {STATIC $_=[];STATIC FUNCTION ADD(STRING $P, CALLABLE $C){SELF::$_['#^' . $P . '$#']=$C;} STATIC FUNCTION RUN(){$R=FILTER_INPUT(INPUT_SERVER,'REQUEST_URI');FOREACH(SELF::$_ AS $P=>$C){IF(PREG_MATCH($P,$R,$PA)===1){ARRAY_SHIFT($PA);CALL_USER_FUNC_ARRAY($C,ARRAY_VALUES($PA));RETURN TRUE;}}RETURN FALSE;}}
 
	/*
		Autor - Regz.pl
 
		Przykład:
			ROUTER::ADD('/', FUNCTION() { echo 'Homepage'; })
			ROUTER::ADD('/forum/', FUNCTION() { echo 'Forum'; })
			ROUTER::ADD('/forum/([0-9]+)/', FUNCTION($ID) { echo 'Forum ID: ' . $ID; })
			ROUTER::ADD('(.*)', FUNCTION() { echo 'Error 404'; });
			ROUTER::RUN();
	*/
