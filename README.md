# qMagic
public class QMatic implements Runnable { 
private int orderNo; 	
public QMatic() { this.orderNo = 0; 	}
	
@Override public void run() { 		
// a little bit delay to see race condition! ThreadSleeper.sleep(50); 		
// Critical section for all threads! this.orderNo = this.orderNo + 1; 		
StringBuilder builder = new StringBuilder(); 		
builder.append(Thread.currentThread().getName());
builder.append(" thread got "); builder.append(this.orderNo); builder.append(" from Qmatic!"); 
		System.out.println(builder.toString());
	}
}
