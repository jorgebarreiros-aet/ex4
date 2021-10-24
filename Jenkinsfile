
node{
stage('CheckoutSCM'){
	def resp
	try{
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
	if (resp=='3') {
		echo 'Well done, genius!'
		}
	else {
		throw new Exception("Throw to stop pipeline") 
		}
	}
	}
	catch(exp){
		echo 'You are truly exceptional!'
		}
   }
}
