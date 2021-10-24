
node{
stage('Math is hard'){
	def resp
	try{
    retry(3){
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
		throw new Exception("Oh boy...") 
		}
	}
	}
	catch(exp){
		echo 'You are truly exceptional!'
		}
   }
}
