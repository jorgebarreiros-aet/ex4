
node{
stage('CheckoutSCM'){
    retry(5){
    try{
    timeout(time: 30, unit: 'SECONDS') {
          resp = input message: '1+2=?', 
		               parameters: [string(defaultValue: '0', 
			                          description: 'Response', 
			                          name: 'response', 
			                          trim: true)]
		}
    }
   catch(except){
      resp='0';
   }
	if resp=='3' {
		echo 'Well done, genius!'
		return true
		}
	return false
	}
   echo 'Gotta go, Einstein, see you around!'
   }
}
